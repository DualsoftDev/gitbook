# Case4 : ApiCall → Tag → ApiDef

#### 1. 개념 소개

DS 시스템에서 **Tag**는 시스템 간 데이터 전달을 위한 핵심 인터페이스입니다. 이 Tag는 일반적으로는 **Active 시스템이 WriteTag를 Write, Passive 시스템이 ReadTag를 Read**하는 구조로 사용되며, 이 구조는 \*\*1:1 연결(Pair)\*\*을 전제로 합니다.

그러나 일부 예외적 구성(예: Shared Memory, 중앙 DB 기반 연동)에서는 **Tag가 동시에 여러 시스템에 의해 Read와 Write 가능한 공유 구조**처럼 작동하며, 이때 Tag는 구조적 제약을 넘어서 실행 단계에서의 **이중성**을 나타냅니다.

> ⊕ 이중성 핵심: **Tag는 구조적으로는 ReadTag-WriteTag Pair이지만, Tag를 Share할 경우 Read/Write 이중성이 발생할 수 있음**

***

#### 2. 구조적 정의: 1:1 Pair <a href="#user-content-2-11-pair" id="user-content-2-11-pair"></a>

```
[Active System] → (Write Tag) →(물리전송)→ (Read Tag) → [Passive System]
```

***

#### 3. Shared 구조에서의 Read/Write 이중성 <a href="#user-content-3-shared-readwrite" id="user-content-3-shared-readwrite"></a>

**▸ Shared Memory 기반**

* 여러 시스템이 동일 메모리 주소를 사용하여 Tag를 동시에 읽고 쓸 수 있음
* Active/Passive 구분 없이 **Tag를 공유 변수처럼 활용**

**▸ DB 기반 연동 구조**

* Tag가 DB Row에 매핑되어, 다수의 시스템이 값을 조회/갱신 가능
* 논리적으로 동일 Tag지만, 동기화가 필요하며 이중 접근 허용

| 조건            | Read/Write 가능 여부 | 설명                         |
| ------------- | ---------------- | -------------------------- |
| 기본 구조         | ❌                | Write → Read 1:1 구조 (Pair) |
| Shared Memory | ✅                | 공유 변수처럼 다수 접근 가능           |
| DB 매핑 구조      | ✅                | 간접 경로로 다수 시스템이 접근 가능       |

> 위의 예외적 사용은 DS의 외부 확장으로 간주되며, 설계상 일관성과 충돌 방지를 위한 동기화가 필수입니다.

***

#### 4. 반복 연결 구조에서의 해석 <a href="#user-content-4" id="user-content-4"></a>

```
ApiCall → Tag → ApiDef → Work → Call → ApiCall → Tag → ApiDef → ...
```

* 위 구조처럼 Tag는 시스템 간 반복되는 호출 흐름의 중심입니다.

***

#### 5. 정리 <a href="#user-content-5-2" id="user-content-5-2"></a>

* **Tag는 구조적으로는 ReadTag/WriteTag 1:1 연결된 Pair 구조**입니다.
* Shared 구조에서는 ActiveSystem은 WriteTag로 해석 PassiveSystem은 ReadTag로 해석 하는 이중성이 나타납니다.
* DS 시스템은 명확한 흐름 해석을 위해 기본적으로 Pair 구조를 권장하되, 외부 연동 시스템과의 확장을 통해 Tag의 이중성이 실제 운용에서 현실화될 수 있음을 고려해야 합니다.
