# 🧪 VR Social Bias Experiment (Research Project)



> **Project Duration:** 2025.11 ~ 2026.01 (Expected)  
> **Client:** Monash University (Research Team led by Rigissa Megalokonomou)  
> **Developer:** 이창연, 나우진, Kasey Main

##  Overview

본 프로젝트는 **성별(Gender)과 인종(Ethnicity)에 따른 사회적 차별과 편견을 연구**하기 위한 가상현실(VR) 실험 어플리케이션입니다.

참가자는 가상 카페 환경에서 다양한 인종과 성별을 가진 4명의 아바타와 상호작용하며, 연구팀은 이 과정에서 발생하는 참가자의 **시선(Eye-tracking)**, **동공 확장(Pupil dilation)**, **의사결정 데이터**를 수집하여 분석합니다.

---

## Target Hardware & Tech Stack

본 프로젝트는 데이터 수집을 위해 **Eye-tracking**과 **Facial Expression** 감지가 가능한 HMD에 최적화되어 개발됩니다.

* **Engine:** Unity 3D 
* **Primary Device:** Meta Quest Pro (Eye & Face Tracking enabled)
* **Key SDKs:**
    * Meta XR SDK for Eye/Face Tracking
    * Custom Data Logging System (CSV/JSON Export)
      
---

##  Experiment Workflow

실험은 참가자의 편견 없는 반응을 이끌어내기 위해 통제된 4단계 시퀀스로 진행됩니다.

### 1. Introduction & Neutral Room
* 중립적인 가상 공간에서 실험의 목적과 진행 방식에 대한 텍스트 가이드를 제공합니다.

### 2. The Cafe Scene (Interaction Phase)
* **환경:** 일상적인 소음과 배경 NPC가 존재하는 카페 환경.
* **진행:** 4명의 서로 다른 아바타(인종/성별 조합)가 무작위 순서(Random Order)로 등장.
* **상호작용:** 각 아바타는 1~2분 분량의 스크립트(무작위 배정)를 낭독합니다.
* **평가:** 아바타 퇴장 후, 컨트롤러 또는 시선(Gaze)을 사용하여 4개의 객관식 질문에 답변합니다.

### 3. Ranking Phase
* 중립 공간으로 이동하여 이전에 만난 4명의 아바타 얼굴을 확인합니다.
* **선호도** 및 주의 집중도에 따라 아바타의 순위를 매깁니다 (1~4위).

### 4. Trust Game (Investment Phase)
* **경제적 행동 실험:** 참가자는 $5의 예산을 부여받습니다.
* 4명의 아바타를 다시 무작위 순서로 만나, 각 아바타에게 **얼마를 공유(투자)할지 결정**합니다.
* 이 데이터는 참가자의 무의식적인 신뢰도를 측정하는 지표로 활용됩니다.

---

##  Data Collection Pipeline

연구의 핵심인 데이터 로그 시스템은 다음 항목들을 프레임 단위로 기록하여 `.csv` 형식으로 추출합니다.

| Data Type | Description | Frequency |
| :--- | :--- | :--- |
| **Gaze / Eye Tracking** | 아바타의 특정 부위(눈, 입, 몸 등)에 머문 시간 및 시선 궤적 | Real-time (60Hz+) |
| **Decision Making** | 퀴즈 답변, 선호도 랭킹, Trust Game 투자 금액 | Per Event |
| **Interaction Time** | 각 섹션별 소요 시간 및 응답 반응 속도(Latency) | Per Event |

---


##  Confidentiality & License

* 본 프로젝트는 **Monash University**와의 계약에 의거하여 수행되는 연구 과제입니다.
* 소스 코드의 일부 로직과 실험 데이터는 비공개로 관리합니다.
