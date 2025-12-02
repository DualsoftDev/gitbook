# Case1 : System ⊕ Device

### 1. 개념 소개

DS 시스템은 특정 상황에 따라 "System" 또는 "Device" 역할을 수행할 수 있으며, 이 두 가지는 배타적이지 않고 동적으로 전환됩니다. 이를 **System ⊕ Device 이중성**이라 합니다.

* **System**: 외부 시스템에 명령을 보내는 능동적 실행 주체
* **Device**: 외부에서 호출받아 응답하는 수동적 실행 대상

> ⊕ (XOR, 베타적  논리합): 동일 시점에는 하나의 역할만 수행하되, 전환은 가능함

<div align="center" data-full-width="true"><figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption><p>XOR</p></figcaption></figure></div>

### 2. 두 가지 역할 정의 <a href="#user-content-2" id="user-content-2"></a>

#### **2.1 System (Active System)**

* **정의**: 다른 시스템을 호출하고 실행 흐름을 주도하는 주체
* **대표 행위**: `ApiCall`을 사용하여 외부의 `ApiDef` 호출
* **특징**:
  * 외부 제어 흐름을 개시함
  * 요청/응답에 대한 책임을 가짐

#### **2.2 Device (Passive System)**

* **정의**: 외부로부터 호출되어 동작하는 대상 시스템
* **대표 행위**: `ApiDef`를 통해 외부 요청에 반응함
* **특징**:
  * 내부 FSM 흐름을 포함할 수 있음
  * 외부에서는 내부 로직을 직접 제어할 수 없음

### 3. 이중성 원리 <a href="#user-content-3" id="user-content-3"></a>

#### **3.1 동적 역할 전환**

```
[상황 1]
A.ApiCall → B.ApiDef
→ A = System (능동 호출)
→ B = Device (응답 수신)

[상황 2]
B.ApiCall → A.ApiDef
→ B = System (능동 호출)
→ A = Device (응답 수신)
```

#### **3.2 수평적 구조**

* 시스템 간 호출 관계는 부모-자식이 아닌 형제 구조
* 호출 방향에 따라 역할이 유동적으로 변함

### 4. 실생활 예시 <a href="#user-content-4" id="user-content-4"></a>

**제조 자동화 시스템**

* **컨베이어 (A)** → 로봇팔 (B): 제품 전달 요청 → A는 System, B는 Device
* **로봇팔 (B)** → 컨베이어 (A): 픽업 완료 알림 → B는 System, A는 Device

### 5. 구현 구조 <a href="#user-content-5" id="user-content-5"></a>

#### **5.1 호출 흐름**

```
System A
  └─ ApiCall ──▶ System B
                    └─ ApiDef
```

#### **5.2 흐름 요약**

* ApiCall 보내는 쪽 → System (능동)
* ApiDef 응답하는 쪽 → Device (수동)
* 하나의 시스템이 두 역할을 모두 가질 수 있음 (단, 동시에 수행하지는 않음)

### 6. 주의사항 <a href="#user-content-6" id="user-content-6"></a>

#### **6.1 순환 호출 가능성**

```
A.ApiCall → B.ApiDef
B.ApiCall → A.ApiDef
```

* 정상적으로 작동할 수 있으나, Deadlock 가능성 주의 필요
* 순환 경로 발생 시 경고 메시지 제공이 바람직

#### **6.2 상태 가시성**

* 외부에서 Device의 상태는 `ApiDef` 응답 로그로만 유추 가능
* 내부 FSM 흐름은 직접 관찰 불가

#### **6.3 내부 Controller 존재**

* Device도 내부적으로는 항상 Controller(FSM 등)를 갖고 있음
* 단지 외부에서 접근할 수 없는 것뿐

### 7. 설계 고려사항 <a href="#user-content-7" id="user-content-7"></a>

* **명확한 흐름 설계**: 각 System이 언제 어떤 역할을 수행할지를 명시
* **Deadlock 예방**: 무한 루프 가능성 있는 경로 사전 탐지
* **디버깅 전략**: 각 ApiCall/ApiDef의 상태 로그 분석 및 시각화 필요

### 8. 정리 <a href="#user-content-8" id="user-content-8"></a>

DS의 **System ⊕ Device 이중성**은 시스템 간 동적 호출 구조를 수평적이고 유연하게 구성할 수 있게 해줍니다.

* 하나의 시스템이 상황에 따라 두 역할을 오가며 작동
* 호출 흐름은 명확히 설계되되, 실행 중 동적으로 전환 가능
* 외부-내부 구조 분리로 재사용성과 안정성을 확보
