---
icon: list-tree
---

# DS 모델링 방법

## 예제 1. 복동실린더

### 1. 개요

이 문서는 DS 시스템에서 **실린더**를 모델링하는 방법에 대해 설명합니다. 실린더는 물리적 장치(실린더, 솔밸브, 센서)와 논리적 구성 요소(Work, Action)로 모델링되며, I/O 맵과 연결되어 동작합니다.

***

### 2. 물리 디바이스 구성

* **실린더 (1EA)**
  * 동작 방향: 전진(ADV), 후진(RET)
  * I/O:
    * **Input**: 센서(전/후진)
    * **Output**: 솔밸브(전/후진)
* **솔밸브 (2개)**
  * 전진 솔밸브
  * 후진 솔밸브
* **센서 (2개)**
  * 전진 센서
  * 후진 센서

<figure><img src="../../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

***

### 3. DS 모델 구성

#### 🔷 Work 단위 구성

* 하나의 실린더 동작은 Work 단위로 표현되며, 각 동작(전진/후진)을 Action으로 모델링합니다.
*   **Work 내부 구성 예시**:

    ```
    실린더.ADV → 실린더.RET 
    ```
* 각 Action은 센서 신호( Input)와 솔밸브 신호(Output)를 통해 **동작의 시작과 완료 조건**을 정의합니다.

<figure><img src="../../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

#### 🔶 모델링 원칙

* 실린더의 각 동작(전진/후진)을 Action으로 정의합니다.
* 화살표로 동작 순서를 명시합니다 (예: 전진 후 후진).
* Work 및 Action은 **그룹(Group)** 으로 묶여야 합니다.

> 💡 그룹화 시, DS 도구의 “그룹 지정” 기능을 사용해야 합니다.

***

### 4. Device I/O 매핑

|       Name      | DataType |  Input | Output |
| :-------------: | :------: | :----: | :----: |
| sample\_실린더.ADV |   bool   | P00000 | P00040 |
| sample\_실린더.RET |   bool   | P00001 | P00041 |

* 각 Action에 대응되는 **센서 입력 (Input)** 과 **솔밸브 출력 (Output)** 주소를 할당합니다.
* 실제 제어 시스템에서 사용하는 **PLC(LS XGK) 주소 (Pxxxx)** 와 연동됩니다.

***

### 5. 요약 및 주의사항

* 모든 실린더 동작은 Work 및 Action 단위로 표현되어야 하며, 반드시 순서를 지정해야 합니다.
* 각 Action의 입력과 출력은 Device I/O Table에 명확히 정의되어야 합니다.
* 그룹 지정이 누락되면 DS에서 동작 순서를 인식하지 못할 수 있으므로, 필수로 그룹화하십시오.
