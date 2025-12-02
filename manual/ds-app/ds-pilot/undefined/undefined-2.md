---
description: (공정별 동작 편차 시각화 도구)
---

# 편차 분석

## 📘 히트맵 차트 매뉴얼

<figure><img src="../../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

### 1️⃣ 기능 개요

히트맵(Heatmap) 차트는 각 공정의 **사이클별 동작 시간 편차**를 시각적으로 표현한 분석 도구입니다.\
시간 흐름에 따른 **공정의 일관성**, **불안정성**, **편차 패턴**을 빠르게 파악할 수 있습니다.

***

### 2️⃣ 주요 분석 항목

히트맵 차트를 통해 다음과 같은 내용을 쉽게 진단할 수 있습니다:

<table><thead><tr><th width="283.99993896484375" align="center">분석 항목</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center">공정 간 편차 비교</td><td align="center">특정 공정이 다른 공정보다 <strong>시간 분포 편차가 큰지</strong> 판단</td></tr><tr><td align="center">사이클 간 시간 차이</td><td align="center">공정 수행 시간이 <strong>일정한지 또는 불규칙한지</strong> 분석</td></tr><tr><td align="center">그룹/시간대 흐름 이상</td><td align="center">특정 시간대 또는 그룹에서 <strong>패턴이 일관되지 않는지</strong> 식별</td></tr></tbody></table>

***

### 3️⃣ 히트맵 차트 해석

#### 🔢 각 셀의 수치

* 값 범위: `0.0 ~ 1.0`
* 의미: **편차 정규화 수치**
  * `0`에 가까울수록 → **안정적인 수행**
  * `1`에 가까울수록 → **편차가 크고 불안정**

***

#### 🎨 색상 표현

<table><thead><tr><th width="167.6666259765625" align="center">색상계열</th><th width="176.666748046875" align="center">값 범위</th><th align="center">의미</th></tr></thead><tbody><tr><td align="center">🔵 청색</td><td align="center">0.0 ~ 0.1</td><td align="center">매우 안정적</td></tr><tr><td align="center">🟢 연두</td><td align="center">0.2 ~ 0.4</td><td align="center">평균 이하</td></tr><tr><td align="center">🟠 주황</td><td align="center">0.6 ~ 0.8</td><td align="center">편차 주의</td></tr><tr><td align="center">🔴 붉은색</td><td align="center">0.9 ~ 1.0</td><td align="center">매우 불안정</td></tr><tr><td align="center">🟣 분홍</td><td align="center">1.0 이상</td><td align="center">편차 극심 (스케일로 인해 보정된 이상값 포함)</td></tr></tbody></table>

***

### 4️⃣ \[Scale X] 슬라이더 사용법

#### 기능 목적

* 데이터 정규화 보정
* 전체 편차 값의 상대적 차이를 명확하게 구분

#### 동작 방식

* 슬라이더를 이동하면 **각 편차 값 × Scale X 값**으로 재보정
* 예:
  * 원래 편차값: 0.3
  * Scale X: 2 → 보정값: 0.6
  * 시각적으로 더 강조됨

***

### 5️⃣ 활용 팁

* 공정 흐름 최적화 시:
  * 편차가 큰 공정부터 원인 분석하여 개선 우선순위 설정
* 야간·주간 시간대 비교:
  * 시간대별 이상 패턴(불규칙 수행) 여부 시각적으로 파악
* 사이클 자동화 기준 설정 전:
  * 안정된 구간을 기준으로 동기화/제어 포인트 정의

***

### 6️⃣ 실무 적용 사례

<table><thead><tr><th width="157" align="center">공정명</th><th width="198.3333740234375" align="center">문제 유형</th><th align="center">개선 포인트</th></tr></thead><tbody><tr><td align="center">S301_WELD</td><td align="center">야간 편차 ↑</td><td align="center">야간 인원/센서 감도 확인</td></tr><tr><td align="center">S302_LOAD</td><td align="center">전체 편차 ↑</td><td align="center">로봇 속도 조정, 원점 지연 발생 여부 확인</td></tr><tr><td align="center">S303_WAIT</td><td align="center">편차 거의 없음</td><td align="center">기준 사이클 설정용 참조 공정으로 활용 가능</td></tr></tbody></table>

### 7️⃣ 유의사항

* 정규화 값은 평균 기준이므로, **절대 시간이 아닌 상대적 편차**를 의미합니다.
* 값이 크다고 반드시 문제는 아니며, **다른 공정/구간과의 비교가 핵심**입니다.
* 값이 1.0을 초과하는 경우는 Scale X 값에 따른 **시각적 확대**로, 본질적 오류는 아님
