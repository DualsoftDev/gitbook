---
icon: l
---

# 라이선스 정책

## 📘 Dualsoft 라이선스 정책 매뉴얼

{% hint style="success" %}
**Dualsoft**의 **AAS Runtime 플랫폼**은 제조 **디지털 트윈** 환경을 위한 강력한 솔루션으로,&#x20;

사용 Dualsoft의 **AAS Runtime 플랫폼**은 제조 산업의 디지털 트윈 구현을 위한 **모델 기반 자동 제어 및 시뮬레이션 도구**입니다.\
사용 목적에 따라 다음 두 가지 라이선스로 제공됩니다:
{% endhint %}

<table><thead><tr><th width="308" align="center">버전</th><th align="center">설명</th></tr></thead><tbody><tr><td align="center"><strong>Community</strong> (무료)</td><td align="center">모델링 및 시뮬레이션 중심의 개인/교육용 버전</td></tr><tr><td align="center"><strong>Professional</strong> (유료)</td><td align="center">상업적 활용, 실시간 연동, 모니터링 기능 포함</td></tr></tbody></table>

### 🧩 1. DS Apps 라이선스 기능 비교

<table data-full-width="false"><thead><tr><th align="center">이 름</th><th align="center">기 능</th><th width="150.0001220703125" align="center">Community (무료)</th><th width="150" align="center">Professional (유료)</th><th width="248" align="center">비 교</th></tr></thead><tbody><tr><td align="center">PowerPoint Add-in</td><td align="center">Control Code Generation</td><td align="center">✅</td><td align="center">✅</td><td align="center">제어코드 자동생성(PLC/PC)</td></tr><tr><td align="center"></td><td align="center">Simulation</td><td align="center">✅</td><td align="center">✅</td><td align="center">시뮬레이션 검증</td></tr><tr><td align="center"></td><td align="center">Virtual Logic</td><td align="center">✅</td><td align="center">✅</td><td align="center">가상 제어 모드</td></tr><tr><td align="center"></td><td align="center">Virtual Plant</td><td align="center">✅</td><td align="center">✅</td><td align="center">가상 물리 모드</td></tr><tr><td align="center">DS Pilot</td><td align="center"></td><td align="center">❌</td><td align="center">✅</td><td align="center">데이터 모니터링 및 분석</td></tr></tbody></table>

📌 **DS Pilot App은 Professional에서만 제공**

### 🧩 2. DS Runtime SDKs 기능 비교&#x20;

|         기능        | Community (무료) | Professional (유료) |
| :---------------: | :------------: | :---------------: |
|   Simulation API  |        ✅       |         ✅         |
|    Control API    |        ✅       |         ✅         |
| Virtual Logic API |        ✅       |         ✅         |
| Virtual Plant API |        ✅       |         ✅         |
|    Monitor API    |        ❌       |         ✅         |

📌 **Monitor API는 예지 보전 및 실시간 데이터 활용 시 필수**

### ✔️ 3. 라이선스별 기능 요약

#### 🆓 Community (무료)

* **PowerPoint Add-in**: 직관적인 AAS 모델 설계 도구
* **DS Runtime SDK**: Simulation / Control / Logic / Plant API 지원
* **DS Pilot App / Monitor API 미제공**

#### 💼 Professional (유료)

* 모든 Community 기능 포함
* **DS Pilot App** 제공
  * 공정 상태 실시간 시각화 앱
  * **모니터 대상 IP 별 라이선스 부여**
* **Monitor API (Passive Mode)** 제공
  * 예지 보전 및 실시간 모니터링에 활용
* **확장 가능한 API 커스터마이징** 가능

### 🛠️ 4. Customizing 기반 개발 및 배포 시나리오

> DS 플랫폼을 활용한 실제 **산업용 적용 절차**

### ⚠️ 유의사항

* `DS Pilot App`과 `Monitor API`의 **커스터마이징은 Professional에서만 허용**
* 모니터링 기능은 **설비별 IP 단위로 라이선스 부여됨**
* 모든 라이선스 관련 문의 및 구매는 **DUALSOFT 공식 채널**로 문의



### ✅ 요약표

|         항목        | Community | Professional |
| :---------------: | :-------: | :----------: |
| PowerPoint Add-in |     ✅     |       ✅      |
|      제어 코드 생성     |     ✅     |       ✅      |
|       시뮬레이션       |     ✅     |       ✅      |
|     가상 제어/플랜트     |     ✅     |       ✅      |
|  **DS Pilot App** |     ❌     |       ✅      |
|  **Monitor API**  |     ❌     |       ✅      |
|     커스터마이징 가능     |    제한적    |     전체 가능    |



### 🔔Customizing 기반 개발 및 배포 시나리오

{% hint style="success" %}
Dualsoft SDK는 커스터마이징(Customizing)을 통해 산업별 특화 기능 구현이 가능합니다.\
단, **Monitor API 및 DS Pilot App의 커스터마이징은 Professional(유료) 라이선스 기반**에서만 허용됩니다.
{% endhint %}

#### 1. 설계 및 모델링 <a href="#user-content-1" id="user-content-1"></a>

* PowerPoint Add-in을 이용한 공정 설계 및 AASX 기반 모델 정의

#### 2. 로직 구성 및 테스트 <a href="#user-content-2" id="user-content-2"></a>

* DS Runtime SDK를 활용한 Sequence 제어 로직 및 API 테스트
* 시뮬레이션, 가상 제어, 논리 검증 등을 API 기반으로 구현

#### 3. 통합 및 검증 <a href="#user-content-3" id="user-content-3"></a>

* OPC UA 또는 REST API 기반의 외부 연동 및 상태 데이터 수집
* 가상 환경과 실제 설비 데이터를 비교 분석

#### 4. 배포 및 운영 <a href="#user-content-4" id="user-content-4"></a>

* 상용 라이선스를 통해 Monitor 기능 및 DS Pilot App 활성화
* 현장 실시간 연계 기반의 운영 시스템 구축

{% hint style="warning" %}
**DS Pilot App Customizing은 상용 환경에서만 제공되며, IP 단위 라이선스 정책이 적용됩니다.**
{% endhint %}



## 사용 조건

{% hint style="info" %}
## 본 소프트웨어(이하 "소프트웨어")의 실행 파일, 라이브러리, 문서 및 기타 구성 요소는 다음 조건 하에 사용할 수 있습니다. 본 소프트웨어는 바이너리 형태로 제공됩니다.

1. 사용 허가   \
   소프트웨어는 개인적, 비상업적, 연구 목적 또는 공식 API(SDK 포함)를 통한 상업적 용도의 실행을 위해 자유롭게 설치 및 사용할 수 있습니다. 단, 소프트웨어의 수정 및 재컴파일은 허용되지 않습니다.
2. 상업적 재배포 금지   \
   소프트웨어 또는 그 일부를 상업적 목적으로 재배포, 판매, 임대, 라이선싱하는 행위는 명시적으로 금지됩니다. 단, DualSoft Inc.의 사전 서면 동의를 받은 경우는 예외로 합니다.
3. 공식 API 사용   \
   소프트웨어가 제공하는 공식 API(SDK 포함)를 통한 기능 접근 및 사용은 어떠한 목적이든 허용됩니다(상업적 목적 포함). 단, API를 변조하거나, 비공식 수단을 통해 소프트웨어의 내부 구조나 동작에 접근하는 행위는 금지됩니다.
4. 리버스 엔지니어링 금지   \
   사용자는 소프트웨어를 디컴파일, 리버스 엔지니어링, 디스어셈블하거나, 이와 유사한 방식으로 분석 또는 재구성할 수 없습니다.
5. 저작권 및 고지 유지   \
   소프트웨어 또는 그 일부를 사용하는 경우, 상단의 저작권 고지 및 본 라이선스 전문을 그대로 유지해야 합니다. 소프트웨어의 기능을 참조하거나 연동하여 개발한 파생 제품의 경우에도 본 라이선스의 조건을 준수해야 합니다.
6. 면책 조항   \
   본 소프트웨어는 "있는 그대로(as-is)" 제공되며, 상품성, 특정 목적에의 적합성, 오류 없는 동작, 제3자 권리 비침해 등에 대해 어떠한 명시적 또는 묵시적 보증도 제공하지 않습니다. 소프트웨어의 사용 또는 사용 불능으로 인해 발생하는 모든 직·간접적 손해에 대해 DualSoft Inc.는 책임지지 않습니다.
7. 준거법   \
   이 라이선스는 대한민국 법률에 따라 해석되고 집행됩니다.



_Copyright (c) 2019 Dualsoft. All Rights Reserved._
{% endhint %}
