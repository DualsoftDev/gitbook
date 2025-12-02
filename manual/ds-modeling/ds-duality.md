# DS Duality 이중성 개요

### 1. 개요 <a href="#user-content-1" id="user-content-1"></a>

DS(Dualsoft) 시스템은 복잡한 산업 자동화 환경에서 유연하고 확장 가능한 시스템 설계를 위해 **이중성(Duality)** 개념을 핵심 설계 원리로 채택합니다. 이중성이란 **하나의 구성 요소가 맥락에 따라 역할과 의미가 달라지는 설계 구조**로, 모듈화 및 재사용성, 시스템 간 연결성, 동적 해석 가능성을 극대화합니다.

이중성은 크게 두 가지 범주로 나뉩니다:

{% hint style="info" %}
* **구조적 이중성 (Structural Duality)**: 시스템 구성 요소 간의 설계 및 역할 분리와 관계
* **실행적 이중성 (Execution Duality)**: 실행 시점에서의 상태 변화, 신호 감지, 인과 흐름의 해석
{% endhint %}

***

### 2. 이중성의 핵심 원리 <a href="#user-content-2" id="user-content-2"></a>

1. **동적 역할 전환**: 동일한 객체라도 호출 방향, 관찰 관점, 흐름 조건에 따라 다른 역할 수행
2. **관계 기반 해석**: 객체 자체보다 인과 연결(Arrow)과 주변 관계에 따라 해석
3. **계층적 추상화**: Bit → Call → Work → System → Project 구조로 확장
4. **반복 가능한 흐름 구조**: `ApiDef → Work → Call → ApiCall → ApiDef → ...` 구조가 순환됨

***

### 3. 구조적 이중성 요약  <a href="#user-content-3-cases-14" id="user-content-3-cases-14"></a>

<table><thead><tr><th width="67">Case</th><th width="212">구성 요소</th><th>이중성 설명</th></tr></thead><tbody><tr><td>1</td><td>System ⊕ Device</td><td>호출 방향에 따라 능동적/수동적 역할 수행</td></tr><tr><td>2</td><td>Instance ⊕ Reference</td><td>실행 실체와 참조 대상을 구분하며 설계-사용 분리</td></tr><tr><td>3</td><td>원인(Bit) ⊕ 결과(Bit)</td><td>Bit는 흐름 속에서 원인이자 결과로 해석됨</td></tr><tr><td>4</td><td>ReadTag ⊕ WriteTag</td><td>호출자와 응답자가 맥락에 따라 읽기쓰기 해석됨</td></tr></tbody></table>



### 4. 이중성 설계가 주는 효과

#### ▸ 설계 측면 <a href="#user-content" id="user-content"></a>

* 명확한 구성 요소 정의와 재사용성 향상
* 설계-실행 간의 추상화 경계 확립

#### ▸ 실행 측면 <a href="#user-content" id="user-content"></a>

* 흐름 해석의 명시성과 자동화 가능성 향상
* 상태 기반의 제어 로직 설계 용이

#### ▸ 시스템 통합 측면 <a href="#user-content" id="user-content"></a>

* 계층 간 결합도 감소 및 상호 운용성 강화
* 분산 실행과 참조 기반 설계의 공존 가능

***

### 5. 이중성 설계 원칙 요약 <a href="#user-content-6" id="user-content-6"></a>

* **Bit는 고정된 구조체가 아니라 흐름의 관찰점**
* **모든 구성은 흐름(Arrow) 안에서 원인 ⊕ 결과로 해석됨**
* **ApiDef의 지시 및 관찰 인터페이스 존재 여부가 해석 기준**
* **반복 구조 안에서 구조적, 실행적 이중성이 함께 순환됨**
