  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=300&section=header&text=산모%20건강%20데이터%20분석과%20예측&fontSize=45&animation=fadeIn&fontAlignY=38&desc=AI%20기반%20산모%20위험도%20예측%20시스템%20구축&descAlignY=70&descAlign=62"/>
</p>

<h2 align="center">
  <a href="https://docs.google.com/presentation/d/1CXdXO51N49Jm3MBly5phEeGhM8nwgiyJ/edit?usp=sharing&ouid=117478836458658184968&rtpof=true&sd=true">📊 프로젝트 발표 프레젠테이션</a>
</h2>

---

## 📑 목차

- [📌 프로젝트 개요](#-프로젝트-개요)
- [🗓️ 프로젝트 일정](#️-프로젝트-일정)
- [🎯 프로젝트 목적 및 기대 효과](#-프로젝트-목적-및-기대-효과)
- [👥 팀원 및 역할](#팀원-및-역할)
- [🛠️ 기술 스택 (Tech Stack)](#️-기술-스택-tech-stack)
- [📂 데이터 가공 및 전처리 과정](#-데이터-가공-및-전처리-과정)
- [🧠 분석 모델 및 예측](#-분석-모델-및-예측)
- [📊 시각화 및 주요 결과](#-시각화-및-주요-결과)
- [🖼️ 웹 페이지 구성 및 구현](#️-웹-페이지-구성-및-구현)
- [🗂️ 데이터 요약](#️-데이터-요약)
- [📽️ 시연 영상](#-시연-영상)
- [📈 프로젝트 성과 요약](#-프로젝트-성과-요약)
- [🧭 향후 계획 (Roadmap)](#-향후-계획-roadmap)

---

---

## 📌 프로젝트 개요

**산모 건강 데이터 분석과 예측** 프로젝트는 임산부의 건강 지표(나이, 혈압, 혈당, BMI 등)를 바탕으로 위험 수준을 분류하고 조기 경고를 제공하는 AI 기반 건강 분석 플랫폼입니다. 증가하는 고령 출산과 생활 습관 변화 속에서, 산모의 위험 요소를 조기에 예측하여 맞춤형 관리를 가능하게 하는 것이 목표입니다.

---

## 🗓️ 프로젝트 일정

![Timeline](asset/Timeline.svg)<p align='center'>
---

## 🎯 프로젝트 목적 및 기대 효과

- 산모의 건강 지표를 기반으로 **위험도(저위험, 중위험, 고위험) 예측**
- **임신 주차별 패턴 분석**으로 자가 건강 진단 가능
- 산모가 스스로 건강 지표를 모니터링하고 **생활 습관을 개선**하도록 유도
- 위험도에 따른 **맞춤형 건강 가이드** 제공

---

## 팀원 및 역할

| 이름       | 담당 역할 |
|------------|------------|
| **김재원**     | **데이터 수집, 가공, 분석, 시각화** |
| 옥현우     | 프로젝트 일정 수립, 데이터 수집 및 가공 |
| 한충현     | 데이터 수집, 가공, 분석, 시각화 |

---

## 🛠️ 기술 스택 (Tech Stack)

- **데이터 처리 및 분석**  
  `Python`, `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Plotly`, `Scikit-learn`, `StandardScaler`, `RandomForestClassifier`, `LIME`

- **개발 환경**  
  `Jupyter Notebook`, `Visual Studio Code`, `GitHub`

- **데이터 출처**  
  `Kaggle`

- **시각화 도구**  
  `Seaborn`, `Matplotlib`, `Plotly`, `Streamlit`

---

## 📂 데이터 가공 및 전처리 과정

| 문제점 | 해결 방법 |
|--------|-----------|
| 데이터 특성이 부족함 | 키, 몸무게, BMI, 임신 주수 등 파생 특성 추가 |
| 상식 밖 수치 존재 | 15세 미만, 60세 이상 데이터 삭제 |
| 데이터 양 부족 | 파이썬 random 모듈로 샘플 추가 생성 |
| 단위가 국내 기준 아님 | 혈당 (mmol → mg), 체온 (F → °C)으로 변환 |

---

## 🧠 분석 모델 및 예측

- **모델:** `RandomForestClassifier` (앙상블 학습)
- **목표:** 입력된 건강 지표를 기반으로 `RiskLevel` (저위험, 중위험, 고위험) 예측
- **입력 특성:** 나이, 수축/이완 혈압, 심박수, 키, 몸무게, BMI, 임신 주수, 체온, 혈당
- **성능 평가:** `classification_report`, `confusion matrix`, `LIME`을 통한 설명력 확보

---

## 📊 시각화 및 주요 결과

- 데이터 분포, 상관 관계 시각화 (pie chart, heatmap 등)
- 주요 지표별 위험도 시각화 (`age`, `BMI`, `blood pressure` 등)
- `LIME`으로 모델 예측에 영향을 미친 특성 중요도 시각화
- 예측 정확도 및 분류 성능 분석

---

## 🖼️ 웹 페이지 구성 및 구현

- **대시보드:** 사용자 입력 기반 위험도 예측 결과 제공
- **Streamlit 기반 인터페이스:** 누구나 손쉽게 사용할 수 있는 시각화 중심 플랫폼
<img width="481" height="754" alt="sidebar" src="https://github.com/user-attachments/assets/c7eeac7e-ad40-4626-897a-c1bd71624a6c" />

---

## 🗂️ 데이터 요약

- 총 샘플 수: 2,589
- 주요 변수: 나이, 혈압(수축/이완), 혈당, 체온, 심박수, BMI, 임신 주차 등
- 예측 대상 변수: `RiskLevel` (low, medium, high)

---

## 📽️ 시연 영상

[시연 영상 보기 (Google Drive)](https://drive.google.com/file/d/1AxbLzMSTKeDrFxk_ctRXTZLF1e6eg5V9/view?usp=drive_link)

---


## 📈 프로젝트 성과 요약

- 산모의 건강 지표 기반 **정확한 위험도 예측**
- 시각화 및 리포팅 기능을 통한 **자가 진단 환경 제공**
- `LIME` 적용으로 **모델 예측의 설명력 향상**

---

## 🧭 향후 계획 (Roadmap)

- [ ] 다양한 머신러닝 모델 비교 및 하이퍼파라미터 튜닝
- [ ] 산모 커뮤니티와 연계된 실제 사용자 대상 테스트
- [ ] 의료 전문가 자문을 통한 위험도 해석 고도화

---

