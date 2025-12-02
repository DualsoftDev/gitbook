---
icon: diagram-cells
---

# 도형의 의미

### 1️⃣ Work 도형 (사각형)

<figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252FY0Sy8gnnqBezVLeBF7Tm%252Fimage.png%3Falt%3Dmedia%26token%3D9fdfc501-e5c1-4f7d-b7aa-7fdbc9447515&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=b1eb6d8e&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### 🧭 기능

* 공정/서브 시퀀스 단위를 묶는 **기본 단위 블록**
* 내부 **Action 도형을 제어 상태에 따라 실행**
* 내부 수행 상태를 자체적으로 관리 (Relay 동작 기반)

#### 🔄 상태 전이

<figure><img src="../../../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

|     상태     |            설명            |
| :--------: | :----------------------: |
|   `Ready`  |         초기 대기 상태         |
|   `Going`  |     내부 Action 도형 수행 중    |
| `Finished` |       모든 Action 완료       |
|  `Homing`  | 리셋 절차 수행 중 (→ Ready로 복귀) |

> ✅ **수행 중(Going)** 상태에서는 조건이 만족해도 재수행되지 않음 → **반드시 Homing 후 Ready 상태로 돌아와야 재시작 가능**

#### 📌 상태 표시 스타일

|   상태 요소   |             표시 방법             |
| :-------: | :---------------------------: |
|  초기 종료 상태 |    **텍스트에 밑줄 (underline)**    |
| 데이터 전송 제외 | **텍스트에 취소선 (strike-through)** |

### 2️⃣ Action 도형 (타원)

<figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252FWdPVSSuVoomosyRx6YyB%252Fimage.png%3Falt%3Dmedia%26token%3D2fc9aee3-d161-4dc1-b0cf-45652e2bf893&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=90f2a368&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### 🧭 기능

* **실제 장비 제어를 담당**하는 핵심 도형
* 입출력 신호를 실제로 보내고 받는 단위

#### 🔌 동작 방식

1. **출력 신호 발생 (Actuation)**:
   * 지정된 Tag에 `ON` 신호 출력
2. **입력 신호 대기 (Sensor Read)**:
   * 완료 센서 입력이 감지되면 종료

#### 🧩 사용 위치별 의미

| 위치                  | 의미                     |
| ------------------- | ---------------------- |
| Work 내부             | 장비 제어 동작 발생 (출력/입력 처리) |
| Work 외부             | 동작 없음. **조건 센서 값만 감시** |
| Work 내부 + "비활성화 체크" | **동작 없이 센서 감시만 수행**    |



### 3️⃣ 오토프리 Action 도형 (점선 타원)

<figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252F6SKcCeDlIcknQzJGTecj%252Fimage.png%3Falt%3Dmedia%26token%3D2b79deb6-8419-4d27-802d-3d23498e4488&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=98541ef4&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### 🧭 기능

* **자동 운전 조건에서 완료 신호 감시 용도**
* **실제 출력을 발생하지 않음**

#### 🧩 특성

* `Action 속성`에서 **\[AutoFree] 체크** 시 적용
* 점선 외곽으로 표시됨
* **수동 조건에서는 무시됨**

### 4️⃣ Load 도형 (모서리 접힌 사각형)

<figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252FFNHSGz4JgKJ0YeZLUoD8%252Fimage.png%3Falt%3Dmedia%26token%3D3feccc98-22e6-421a-a132-389df023a495&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=9cf60eb2&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### 📦 기능

* **비표준 DS Library**나 외부 스크립트를 로드
* 사용자 정의 Library 등 외부 요소 포함 시 사용

### 5️⃣인터페이스 도형 (오각형)

<figure><img src="https://dualsoft-2.gitbook.io/~gitbook/image?url=https%3A%2F%2F2569009332-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FggzSj7OzpTUPl71JfBtu%252Fuploads%252F0QhIuNUFD2HJMSanN1Of%252Fimage.png%3Falt%3Dmedia%26token%3D894fce90-2806-44df-8489-366471e1e479&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8b9f6d24&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### 🔁 기능

* 외부 API에 연결하거나 export하는 항목 정의
* 외부 시스템에서 호출 가능한 기능을 선언

#### 🧩 예시

* `StartWork`, `ResetAll`, `WriteRecipe` 등의 API 연동 인터페이스 지정

***

### 🔔 도형별 요약표

|        도형       |        설명        |       외형      |
| :-------------: | :--------------: | :-----------: |
|     **Work**    |  실행 단위 블록, 상태 관리 |     ■ 사각형     |
|    **Action**   |     장비 제어 수행     |    ● 실선 타원    |
| **오토프리 Action** |   조건 감시용 Action  |    ○ 점선 타원    |
|     **Load**    |  외부/비표준 라이브러리 포함 | 📄 모서리 접힌 사각형 |
|    **인터페이스**    | API 외부 호출 포인트 지정 |     ⬠ 오각형     |

### ✅ 참고 사항

* 모든 도형은 **연결선**을 통해 순차/병렬 흐름 구성 가능
* DS 모델의 도형 구성은 최종적으로 DS 언어 → PLC 명령어 구조로 변환됨
* **Action**은 반드시 **I/O 설정**을 통해 실제 신호와 연결되어야 실행 가능
