# analog-electronics-design-mosfet-amplifiers-using-ltspice
https://www.udemy.com/course/analog-electronics-design-mosfet-amplifiers-using-ltspice/


# Analog Electronics: Design MOSFET Amplifiers using LTspice — 강좌 정리

> **출처**: Udemy (https://www.udemy.com/course/analog-electronics-design-mosfet-amplifiers-using-ltspice/)
> **강좌명**: Analog Electronics:- Design MOSFET Amplifiers using LTspice
> **부제**: Integrated Circuits: Hands on Lab Based Course — "Learn All about Transistors, Analog Electronics and Hardware Design - 8"
> **강사**: Practical Buddy
> **최종 업데이트**: 2025년 11월 (Last updated 11/2025)
> **언어**: 영어 (영어 자막 자동 제공)
> **분량**: 14개 섹션 · 56개 강의 · 총 12시간 18분
> **평점**: 4.3 / 5 (22개 평가, 311명 수강)
> **카테고리**: IT & Software > Hardware > LTspice
> **태그**: LTspice, Analog Electronics, Analog Circuit Design, Electronics, Hardware

---

## 1. 강좌 개요

MOSFET **DC 분석**을 다루는 1번 강좌(MOS-Fundamentals)에 이어지는 **2번 강좌**입니다. 이 강좌는 MOSFET 소자를 **증폭기(MOSFET Amplifier)** 로 응용하는 데 초점을 맞추며, DC 해석에서 AC/소신호 해석으로 넘어가는 것이 핵심 흐름입니다.

강좌는 **이론 수식 유도 + LTspice 시뮬레이션 검증**을 쌍으로 묶어 전개합니다. 손계산으로 얻은 gm, Av, Zin, Zout 등의 값을 LTspice에서 그대로 재현해 확인하는 구조입니다.

---

## 2. 학습 목표 (What you'll learn)

- 채널 길이 변조(Channel Length Modulation, λ)의 개념
- 트랜스컨덕턴스(gm)의 개념
- MOSFET 증폭기의 바이어싱 기법
- MOSFET의 AC 등가 모델
- MOSFET의 AC 해석 (소신호 해석)
-.Common Source 증폭기
- Common Gate 증폭기
- Common Drain 증폭기
- MOSFET 증폭기 설계 시 고려사항
- 열적 고려사항 및 방열(Heat Dissipation)
- LTspice를 이용한 MOSFET 증폭기 시뮬레이션
- 문제 해결 및 실무 설계 팁

---

## 3. 커리큘럼 (14 Sections / 56 Lectures / 12h 18m)

### Section 1. Introduction — 2 lectures / 8 min
| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Course Overview | 2:42 | 강좌 개요. LTspice를 활용한 실용적 시뮬레이션 기법으로 견고한 증폭기를 설계하는 접근법 |
| 2 | Introduction | 4:59 | LTspice로 MOSFET 증폭기를 설계하며, 소모(depletion)형·증강(enhancement)형 MOSFET, 작동 영역, gm, CG·CS 증폭기 개념을 다룸 |

---

### Section 2. Quick Revision on Basic Concepts of MOSFETs from Course-1 — 5 lectures / 1h 4min
1번 강좌 핵심 내용의 빠른 복습.

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Symbol & Construction of MOSFETs | 8:43 | 소모형/증강형 MOSFET의 회로 기호와 구조. n/p 영역, 실리콘 산화물 게이트 절연층, 게이트 전압이 드레인-소스 채널을 형성하는 원리 |
| 2 | Characteristics of MOSFETs | 12:22 | DMOSFET/EMOSFET의 전이 특성. vgs와 vds가 id를 지배하는 방식, 임계값과 핀치오프의 역할, 데이터시트 수치 |
| 3 | Drain Current Equation & Operating Region of MOSFETs | 15:19 | n 채널/p 채널 소자의 드레인 전류식 유도. 포화 영역 `id = kn(vgs − vth)²`, 선형 영역 식, 커트오프 조건과 영역 판정 기준 |
| 4 | Plotting Characteristics of N-MOS on LTspice | 20:18 | LTspice에서 n 채널 MOSFET의 전이 특성·드레인-소스 특성 플로팅. vgs, vds 스윕으로 임계값·커트오프·선형·포화 영역 확인 |
| 5 | Different Symbolic Representation of MOSFETs | 6:54 | 증강형 MOSFET의 3가지 기호 표현법 정리(가장 흔한 2가지 중심). 드레인·소스·게이트·바디 관계와 n/p 채널에 따른 전류 방향 차이 |

---

### Section 3. Numericals Based on Operating Region of MOSFETs — 2 lectures / 29 min

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Basic Numericals-1 on N-Channel EMOS | 17:07 | 심볼로 n 채널 MOSFET 식별 후 VGS, VDS, Vth로 작동 영역(커트오프/선형/포화) 판정. 실무적 빠른 계산 기법 |
| 2 | Basic Numericals-2 on P-Channel EMOS | 11:47 | p 채널 증강형 MOSFET 계산. 심볼 판별, 소스/드레인 역할 결정, vsg·vsd·임계전압을 이용한 영역 판정 |

---

### Section 4. Channel Length Modulation (λ) — 4 lectures / 1h 5min

핵심: 이상적인 MOSFET의 유한한 출력 임피던스(`rd`)가 어디서 생기는지를 설명하는 섹션.

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Concept of Channel Length Modulation | 30:46 | vds 증가 → 공핍 영역 확대 → 채널 유효 길이 감소 → 강한 전기장으로 id가 미세하게 증가하는 현상 |
| 2 | Effect of CLM on Drain Current Equation | 19:33 | 포화 영역 id 식에 채널 길이 변조 반영: **`Id = ½·μnCox·(W/L)·(VGS − Vth)²·(1 + λVDS)`**. L, L′, 공핍 영역의 관계 |
| 3 | Output Impedance of MOSFET (rd) | 13:27 | **`r0 = 1/(λ·Id)`** 유도. 이상적 곡선 vs 실무 곡선 비교, 유한 출력 임피던스의 기원 |
| 4 | Course Feedback | 0:50 | 강좌 평가 및 개선점 피드백 |

---

### Section 5. Concept of Transconductance (gm) — 4 lectures / 30min

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Transconductance Definition | 10:10 | gm의 정의 — 게이트-소스 전압 변화에 대한 드레인 전류 변화의 비율. MOSFET 증폭기에서 신호 전달의 매개변수 |
| 2 | Transconductance Derivation | 6:15 | 포화 영역 id를 미분해 gm 유도. **`gm = dId/dVgs = 2Id/(VGS − Vth)`**, μnCox(W/L)과의 관계 |
| 3 | Activity on Transconductance | 13:11 | gm이 vgs에 따라 어떻게 변하는지. 임계값 미만에서 gm = 0, 초과 시 선형 상승. 서로 다른 동작점 간 gm 비교 |
| 4 | Course Feedback | 0:50 | 강좌 평가 및 개선점 피드백 |

---

### Section 6. AC Equivalent Model for P-Channel & N-Channel EMOSFETs — 4 lectures / 46min

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | AC Model of N-Channel E-MOSFET | 15:53 | n 채널 증강형 MOSFET의 AC 등가 모델. 포화 조건, 게이트 절단(무한 입력 임피던스), gm·vgs로 제어되는 ID 전류 |
| 2 | AC Model of P-Channel E-MOSFET | 20:31 | p 채널 증강형 MOSFET의 2가지 AC 등가 모델(vsg 기준 / vgs 기준). λ, rd, 소스→드레인 전류 흐름 설명 |
| 3 | PMOS Equations for Different Operating Regions | 9:05 | vgs 기준 AC 모델로 PMOS의 커트오프/선형/포화 영역별 방정식 유도 (vsd, vth 고려) |
| 4 | Course Feedback | 0:50 | 강좌 평가 및 개선점 피드백 |

---

### Section 7. AC Analysis of N-Channel Enhancement MOSFET — 6 lectures / 1h 47min

소신호 등가 모델을 실제 회로에 적용해 입력/출력 임피던스와 전압 이득을 유도하는 구간.

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Intrinsic AC Parameters of N-Channel E-MOSFET | 26:13 | CS 증폭자 형태의 AC 등가 모델에서 소자의 고유 AC 파라미터 도출. 무한 입력 임피던스, 출력 임피던스, 전압 이득 |
| 2 | AC Equivalent Model for Basic MOSFET Circuit | 28:21 | MOSFET 증폭기 전체의 AC 등가 모델. gm, rd, ro와 AC 분석 기본기를 사용하여 입력 임피던스·출력 임피던스·전압 이득 유도 |
| 3 | MOSFET Amplifier with Load Resistor (RL) | 18:00 | 부하 저항 RL을 포함한 AC 분석. RD ∥ RL, vgs = Vin 관계, **`Av = −gm(RD ∥ RL)`** 유도 |
| 4 | Significance of RS in MOSFET Amplifier | 9:29 | 소스 저항 RS의 의미. VGS–ID 피드백에 의한 자기 바이어스(self-bias), AC 이득에 미치는 영향, KVL과 AC 분석 |
| 5 | MOSFET Amplifier with Unbypassed Rs | 24:04 | rs를 우회(bypass)하지 않은 증폭기의 AC 모델. rs를 이득을 결정하는 피드백으로 해석, **`Av = −gm·rd/(1 + gm·rs)`** |
| 6 | Course Feedback | 0:50 | 강좌 평가 및 개선점 피드백 |

---

### Section 8. MOSFET Common Source (CS) Amplifier Numerical — 8 lectures / 1h 57min

**강좌의 핵심 실전 구간.** 하나의 CS 증폭기 문제를 DC 해석 → AC 해석 → LTspice 검증까지 전 과정을 다룹니다.

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Understanding the Question and Given Parameters | 3:23 | 회로도 읽기, 주어진 MOSFET 파라미터 파악, DC/AC 파라미터(드레인 전류, VGS, 입력·출력 임피던스, 이득, gm) 검증 목표 설정 |
| 2 | Calculating DC Parameters | 29:37 | 전압 분배 바이어스로 Vg, Vgs, Id 계산, 포화 영역 동작 확인 |
| 3 | Verifying DC Parameters via Simulation on LTspice | 20:04 | LTspice에서 Vg, Vgs, Id, gm, Vds 검증. **dot model 사용, SPICE directive 활용, vto/vth 처리 및 kp 조정** |
| 4 | Calculating AC Parameters of MOSFET Amplifiers | 42:57 | 커패시터 단축(capacitor shorting) 원리로 회로를 단순화하여 이득, 입력/출력 임피던스 계산 |
| 5 | Verifying Voltage Gain via Simulation | 8:19 | LTspice로 전압 이득 검증 — **10 kHz에서 이득 ≈ −2.7** (입력 10 mV peak-to-peak) |
| 6 | Verifying Input Impedance via Simulation | 6:41 | AC 분석으로 입력 임피던스 검증. **Zin = Vx/Ix**, 결과 **≈ 7.5 MΩ**, 10 Hz~1 MHz 구간에서 일정 |
| 7 | Verifying Output Impedance via Simulation | 5:09 | 주파수별 출력 임피던스 검증 — **10 kHz에서 ≈ 1.875 kΩ** |
| 8 | Course Feedback | 0:50 | 강좌 평가 및 개선점 피드백 |

---

### Section 9. MOSFET Configurations — 3 lectures / 27min

세 가지 기본 구성의 정성적 비교.

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | Common Source Configuration | 10:50 | n 채널 MOSFET의 CS 구성. 입력 게이트-소스, 출력 드레인-소스. **180° 위상 반전**과 전압 이득 |
| 2 | Common Gate Configuration | 10:56 | CG 구성. 입력을 소스에 인가하고 출력은 드레인에서 취출. **위상 반전 없음(0°)**하며 입력 임피던스가 매우 낮음 |
| 3 | Common Drain Configuration | 5:21 | CD 구성. 입력은 게이트-드레인, 출력은 소스-드레인. **이득이 1인 버퍼 증폭기** |

---

### Section 10. Common Gate Amplifier — 1 lecture / 44min

| # | 강의 | 길이 | 내용 |
|---|------|------|------|
| 1 | AC Analysis of Common Gate Amplifier | 44:15 | DC 소스를 단축한 AC 분석으로 CG 증폭기 유도: **`Rin ≈ 1/gm`**, **`Rout ≈ Rd`**, **`Av ≈ gm·Rd`** |

---

### Sections 11–14. (공개 목록 미노출 — 학습 목표 기반 추정)

Udemy 공개 페이지에서 이 4개 섹션의 세부 강의명은 노출되지 않았습니다(전체 56개 중 39개 강의명만 확인). **What you'll learn** 목록과 강좌 로드맵 설명을 근거로 추정되는 구성은 다음과 같습니다.

| 추정 섹션 | 추정 내용 | 근거 |
|-----------|-----------|------|
| 11. Common Drain Amplifier | CD(소스 폴로워) 증폭기의 AC 해석. Av ≈ 1, 높은 입력 임피던스, 낮은 출력 임피던스 검증 | 학습목표 "Common Drain Amplifier". 참고: 동일 강사(Course-3)의 요약 자료에 Zin ≈ 112 kΩ, Zout ≈ 80 Ω 검증 사례가 존재 |
| 12. MOSFET Amplifier Design Considerations / Biasing Techniques | MOSFET 증폭기 설계 고려사항(게인, 대역폭, 안정성), 바이어싱 기법 | 학습목표 "MOSFET Amplifier Design Considerations", "Biasing techniques" |
| 13. Thermal Considerations and Heat Dissipation | 열적 고려사항 및 방열 전략 | 학습목표 "Thermal Considerations and Heat Dissipation", 로드맵 "Thermal Management" |
| 14. Troubleshooting & Practical Design Tips / 마무리 | 문제 해결 및 실무 설계 팁, LTspice 활용 마무리 | 학습목표 "Troubleshooting and Practical Design Tips", "LTspice Simulation" |

> 각 섹션은 앞선 패턴(Content 강의 + Simulation/Verification 강의 + 0:50 Course Feedback)으로 구성됩니다.

---

## 4. 핵심 수식 요약

### MOSFET DC 방정식

| 영역 | 식 |
|------|-----|
| 포화(Saturation) | `Id = ½·kn·(VGS − Vth)²·(1 + λVDS)` |
| 선형(Linear/Triode) | `Id = kn·[(VGS − Vth)VDS − VDS²/2]·(1 + λVDS)` |
| 커트오프(Cutoff) | `VGS < Vth` → `Id ≈ 0` |
| 채널 길이 변조 | `L' = L − ΔL` (ΔL: 공핍 영역 길이) |
| 출력 임피던스 | `r0 = 1/(λ·Id)` |

### 소신호 파라미터

| 파라미터 | 식 | 의미 |
|----------|-----|------|
| 트랜스컨덕턴스 | `gm = dId/dVgs = 2Id/(VGS − Vth)` | VGS 변화 → ID 변화 변환비 |
| 출력 저항 | `ro = rd = 1/(λ·Id)` | 유한 출력 임피던스 |
| 입력 임피던스 | `Zin = R1 ∥ R2 ∥ ∞` (게이트 무전류) | 매우 높음 |

### 증폭기별 특성

| 구성 | 이득 | 입력 임피던스 | 출력 임피던스 | 위상 |
|------|------|---------------|---------------|------|
| **Common Source** | `Av = −gm·(RD ∥ RL ∥ ro)` | 매우 높음 (수 MΩ) | 낮음 (~kΩ) | 180° 반전 |
| **Common Source (RS 비우회)** | `Av = −gm·rd/(1 + gm·rs)` | 매우 높음 | 낮음 | 180° 반전 |
| **Common Gate** | `Av ≈ +gm·Rd` | 매우 낮음 (`≈ 1/gm`) | `≈ Rd` | 반전 없음 |
| **Common Drain** | `Av ≈ 1` (unity) | 매우 높음 | 매우 낮음 | 반전 없음 |

---

## 5. LTspice 실습 기법 (강좌에서 사용한 방법론)

| 기법 | 설명 |
|------|------|
| **Dot model** | `.model` directive로 MOSFET 소자 모델 직접 정의 (VTO, KP 등 지정) |
| **vto/vth 처리** | 실리콘 MOSFET의 임계전압 설정 방법 |
| **kp 조정** | 드레인 전류 계수 조정으로 소자 특성 맞춤 |
| **SPICE Directive** | 회로도에 `.ac`, `.dc`, `.tran` 등 해석 지시자 삽입 |
| **AC Analysis** | `.ac` 해석으로 이득 및 임피던스 주파수 응답 확인 |
| **Transient Analysis** | 10 mV peak-to-peak 입력으로 실제 파형 및 이득 확인 |
| **입력 임피던스 측정** | 테스트 전압 Vx를 인가하고 `Zin = Vx/Ix`로 계산 |
| **출력 임피던스 측정** | 테스트 소스로 출력에 전압 인가 후 전류로 나눠 계산 |
| **특성 플로팅** | vgs / vds 스윕으로 커트오프·선형·포화 영역 시각적 확인 |

---

## 6. 강좌에서 검증한 수치 예시 (Section 8)

| 검증 항목 | 이론값 | 시뮬레이션 결과 |
|-----------|--------|-----------------|
| 전압 이득 (Av) @ 10 kHz | −2.7 | −2.7 확인 |
| 입력 임피던스 (Zin) | 7.5 MΩ | 7.5 MΩ (10 Hz ~ 1 MHz에서 일정) |
| 출력 임피던스 (Zout) @ 10 kHz | 1.875 kΩ | 1.875 kΩ 확인 |

※ 동일 강사의 후속 강좌(Course-3, Advanced MOSFET Circuits) 요약 자료에서 CD 증폭기의 Zin ≈ 112 kΩ, Zout ≈ 80 Ω 검증 사례가 확인되며, CG 증폭기 이득 ≈ 17.7 사례도 있습니다.

---

## 7. 수강 대상 및 선수 조건

### 수강 대상 (Who this course is for)
- FET를 배우고 싶은 학생
- 트랜지스터를 깊이 이해하고 싶은 학생
- 아날로그 전자회로를 깊이 학습하고 싶은 학생
- 아날로그 회로 설계를 배우고 싶은 학생
- LTspice를 활용한 MOSFET 분석·설계
- LTspice를 활용한 MOSFET 회로 실용 응용
- LTspice를 활용한 MOSFET 아날로그 전자회로
- 전자공학 / 전기공학 / biomedical / 계측 공학 엔지니어

### 선수 조건 (Requirements)
| 순서 | 강좌 | 내용 |
|------|------|------|
| 1 | Course-1 | 전류와 DC 회로 기초 |
| 2 | Course-2 | 반도체 기초 |
| 3 | Course-3 | 다이오드와 커패시터 |
| 4 | Course-4 | BJT와 그 응용 |
| 5 | Course-5 | JFET 기초와 응용 |
| 9 | Course-9 (이 강좌 권장 선수) | MOSFET 기초 — N/P 채널 MOSFET의 기호·구조·작동 원리·특성·드레인 전류식 등 |
| - | 실습 | LTspice를 이용한 실电路 시뮬레이션 경험 |

---

## 8. 강좌 로드맵 (공식 설명)

1. **Channel Length Modulation (λ)** — CLM이 MOSFET 동작과 증폭기 설계에 미치는 영향 이해
2. **Transconductance (gm)** — MOSFET 증폭기 성능에서 gm이 결정하는 역할 숙달
3. **AC Analysis of MOSFET** — 소신호 분석 기법으로 MOSFET 증폭기의 AC 동작 규명
4. **Common Source / Gate / Drain 증폭기** — 세 가지 기본 구성의 설계와 동작 탐구
5. **Design Considerations** — 이득, 대역폭, 안정성을 포함한 MOSFET 증폭기 설계의 핵심 고려사항
6. **Thermal Management** — MOSFET 증폭기 회로의 열적 고려사항과 효과적 방열 전략
7. **LTspice Simulation** — LTspice로 MOSFET 증폭기를 시뮬레이션하여 설계를 검증하고 성능 특성 탐구
8. **Troubleshooting and Design Tips** — 문제 해결 인사이트와 MOSFET 증폭기 최적화 팁

---

## 9. 학습 전략 제안

1. **순차 학습**: Section 2(기초 복습) → Section 4(λ) → Section 5(gm) → Section 6~8(AC 해석) 순서로 반드시 순차 진학. 각 단계가 다음 단계의 전제조건입니다.
2. **수식 → 시뮬레이션 병행**: 매 강의마다 손계산 값을 LTspice로 즉시 재현하는 것이 강좌의 핵심 학습 방식입니다.
3. **피드백 강의 활용**: 각 섹션 말미의 0:50 Course Feedback는 짧지만, 다음 강좌로 넘어가기 전 자기 점검 체크포인트로 활용하세요.
4. **확장 경로**: 이 강좌를 마친 뒤에는 동일 강사의 **"Learn Advance MOSFET Circuits: Cascode to Diff Amp on LTSpice"** (12섹션/62강의/15h7m)로 진행하면 캐스코드, 전류 미러, 디-diff 증폭기까지 이어집니다.

---

## 정보 출처 및 참고사항

- **주요 출처**: Udemy 강좌 페이지 (공개 커리큘럼, 강좌 설명, 학습목록, 요구사항)
- **보조 확인**: 동일 강사의 후속 강좌 커리큘럼, 강사 유튜브 채널(Practical-Buddy) shorts 요약
- **확인 제한 사항**: Udemy는 로그인 없이 전체 커리큘럼을 노출하지 않아, 56개 강의 중 39개의 정확한 강의명과 길이를 확인했습니다. Sections 11–14는 강좌의 공식 "What you'll learn" 및 로드맵을 근거로 추정했으며, 해당 부분을 별도로 표기했습니다.
- **_LAST_UPDATED_ 확인**: 강좌 페이지 표시 기준 최종 업데이트는 2025년 11월로, 요청하신 "2025-11" 정보와 일치합니다.

---

*문서 생성일: 2026-10-01*
