# Goal Tracker MVP PRD

## 1. Product Overview

### 제품 한 줄 설명
매일 해야 할 목표를 체크하면, 하루의 완료 기록이 하나의 그림을 채워가며 시각적으로 누적되는 목표 달성 서비스.

### 핵심 컨셉
기존 Habit Tracker가 체크리스트·달력·연속 기록 중심이라면, 이 제품은 **“매일 한 번의 행동이 그림 한 조각을 완성한다”**는 시각적 보상을 중심으로 한다.

예시:

> 목표: 퇴근 전 청소하기  
> 오늘 완료 → 포도 한 알이 채워짐  
> 한 달간 기록 → 포도송이 완성

---

## 2. Background / Problem

습관이나 반복 목표를 만들더라도 사용자는 시간이 지나면서 목표 자체를 잊거나, 기록 행위가 번거로워 지속하지 못한다.

기존 Habit Tracker는 다음과 같은 문제가 있다.

- 목표를 확인하기 위해 앱을 직접 열어야 한다.
- 완료 기록이 단순 체크 표시로 끝나 보상이 약하다.
- 연속 달성(Streak)이 끊겼을 때 실패감이 크다.
- 목표 달성 현황이 숫자와 통계 중심으로 표현된다.
- 기록하는 행위 자체가 또 하나의 할 일이 된다.

따라서 MVP에서는 **“잊지 않도록 다시 불러오고, 최소한의 행동으로 기록하며, 완료 자체가 작은 보상이 되는 경험”**을 검증한다.

---

## 3. Product Hypothesis

### 핵심 가설

> 사용자가 적절한 시점에 목표를 다시 떠올릴 수 있고, 한 번의 액션으로 완료를 기록하며, 그 결과 그림이 점차 완성된다면 반복 행동을 더 오래 지속할 것이다.

### 세부 가설

1. 사용자는 정해진 시간에 알림을 받으면 목표를 더 자주 기억한다.
2. 완료 기록이 1 Tap 수준이면 기록 이탈이 줄어든다.
3. 단순 체크마크보다 그림이 완성되는 방식이 다시 기록하고 싶은 동기를 높인다.
4. 연속 달성보다 누적된 결과를 보여주는 방식이 실패 후 복귀에 더 유리하다.

---

## 4. MVP Goal

MVP의 목적은 완성된 Habit Tracker를 만드는 것이 아니라 다음 질문을 검증하는 것이다.

### Primary Question

> 시각적 완성 경험이 반복 목표의 기록 지속성에 영향을 주는가?

### MVP에서 확인할 행동

```text
목표 생성
↓
알림 수신
↓
오늘 목표 확인
↓
완료
↓
그림 변화 확인
↓
다음 날 다시 기록
```

---

## 5. Target User

### Primary User

매일 또는 정해진 요일마다 반복적으로 해야 하는 일이 있지만 꾸준히 지속하는 데 어려움을 느끼는 사용자.

예시:

- 퇴근 전 책상 정리
- 운동
- 영양제 먹기
- 일기 쓰기
- 영어 공부
- 물 마시기
- 스트레칭
- 독서

### 초기 MVP에서 제외

다음과 같은 목표는 별도 UX가 필요하므로 제외한다.

- 책 30권 읽기
- 여행지 20곳 방문
- 그림 100장 그리기
- 5kg 감량

MVP는 **누적 횟수형 Goal이 아니라 Routine Goal에 집중한다.**

---

## 6. Jobs To Be Done

### Main JTBD

> 해야 할 일을 매일 잊지 않고 실천하고 싶지만, 복잡하게 관리하고 싶지는 않다.

### Supporting Jobs

> 오늘 목표를 했는지 빠르게 기록하고 싶다.

> 내가 얼마나 지속해왔는지 직관적으로 보고 싶다.

> 하루를 놓쳐도 부담 없이 다시 시작하고 싶다.

> 기록할수록 무언가 완성되는 느낌을 받고 싶다.

---

## 7. Core Experience Principle

제품 UX는 다음 세 가지 원칙을 따른다.

### 1. Remember
사용자가 앱을 기억하는 것이 아니라 **서비스가 목표를 다시 떠올려준다.**

### 2. One Tap
완료 기록까지 필요한 행동을 최소화한다.

### 3. Visual Reward
체크 자체보다 **완료 후 변화하는 시각적 결과**를 핵심 보상으로 만든다.

---

## 8. MVP Scope

### P0 — 반드시 포함

#### 8.1 목표 생성

사용자는 하나의 반복 목표를 생성할 수 있다.

입력 항목:

- 목표 이름
- 반복 요일
- 리마인드 시간
- 비주얼 테마

예시:

```text
목표
퇴근 전 청소하기

반복
월 화 수 목 금

알림
18:00

테마
포도
```

MVP에서는 한 사용자당 Goal 1개까지 허용해도 충분하다.

---

#### 8.2 Today Goal

서비스 진입 시 가장 먼저 오늘 목표를 보여준다.

예시:

```text
오늘의 목표

퇴근 전 청소하기

[ 오늘 완료 ]
```

오늘 기록이 완료된 경우:

```text
오늘 완료했어요 ✓
```

---

#### 8.3 Daily Check

오늘 목표를 완료하면 1회 체크할 수 있다.

조건:

- 하루 1회
- 해당 Goal의 반복 요일에만 활성화
- 완료 후 취소 가능
- 과거 날짜 소급 입력은 제공하지 않음

소급 입력을 제공하지 않는 이유는 실제 행동 기록과 이미지 누적의 관계를 명확하게 유지하기 위해서다.

---

#### 8.4 Visual Progress

완료할 때마다 그림의 한 요소가 채워진다.

예시:

```text
○ ○ ○
○ ● ○
● ● ●
```

완료 액션 직후 간단한 채움 애니메이션을 제공한다.

```text
○
↓
색이 차오름
↓
●
```

이 인터랙션을 MVP의 주요 Delight Moment로 정의한다.

---

#### 8.5 Reminder

사용자가 설정한 시간에 목표 리마인드를 제공한다.

예시:

> 퇴근할 시간이네요 🍇  
> 오늘 청소했나요?

CTA:

- 오늘 완료
- 나중에

---

#### 8.6 Progress Summary

누적 상태를 간단하게 보여준다.

MVP에서는 복잡한 통계 대신 다음 정도만 제공한다.

```text
이번 달 12일 완료
```

Streak은 MVP에서 제공하지 않는다.

---

## 9. Information Architecture

```text
Home
│
├─ Goal
│  ├─ Goal title
│  ├─ Visual progress
│  └─ Today check
│
├─ Progress
│  └─ Monthly completion count
│
└─ Settings
   ├─ Repeat days
   ├─ Reminder time
   └─ Goal edit
```

Bottom Navigation 없이 **Single-screen 중심 구조**로 시작한다.

---

## 10. Main User Flow

### 신규 사용자

```text
Landing
↓
Create Goal
↓
목표 입력
↓
반복 요일 설정
↓
알림 시간 설정
↓
Visual 선택
↓
Goal 생성
↓
Home
```

### Daily Flow

```text
알림
↓
목표 확인
↓
오늘 완료
↓
Visual 채움 애니메이션
↓
완료 상태
↓
Home
```

목표는 **알림에서 완료까지 1~2번의 Tap**이다.

---

## 11. Screen Requirements

### 11.1 Home

구성:

```text
오늘
10월 12일 월요일

퇴근 전 청소하기

     ●
   ● ●
 ● ● ○
○ ○ ○ ○

이번 달 8일 완료

[ 오늘 완료 ]
```

---

### 11.2 Goal Creation

필수 입력만 제공한다.

#### Step 1

```text
어떤 목표를 만들까요?

[퇴근 전 청소하기]
```

#### Step 2

```text
언제 할까요?

월
화
수
목
금
토
일
```

#### Step 3

```text
언제 알려드릴까요?

18:00
```

#### Step 4

```text
어떤 그림을 완성할까요?

🍇
🌷
⭐
```

CTA:

```text
[ 목표 시작하기 ]
```

온보딩은 최대 4 Step을 넘기지 않는다.

---

## 12. Interaction Rules

### 완료

사용자가 `오늘 완료`를 누르면:

1. 버튼 Disable
2. 해당 날짜 Completed 상태 저장
3. Visual 한 칸 채우기
4. Animation
5. Success message 표시

예시:

> 오늘도 한 칸 채웠어요 🍇

---

### 완료 취소

사용자가 실수로 완료했을 경우 취소 가능하다.

```text
완료됨 ✓
```

탭하면:

```text
완료를 취소할까요?
```

---

### 목표를 하지 못한 날

기록하지 않은 날짜는 Empty 상태로 남긴다.

```text
● ● ○ ●
```

실패를 강조하는 표현은 사용하지 않는다.

사용하지 않는 표현:

- X
- Failed
- 빨간 경고
- 연속 기록 실패 메시지

---

## 13. Visual Progress Logic

MVP에서는 날짜와 Visual Cell을 1:1 대응한다.

예시:

```text
Day 1 → Cell 1
Day 2 → Cell 2
Day 3 → Cell 3
...
Day 30 → Cell 30
```

Day 3 미완료:

```text
● ● ○ ● ●
```

해당 Cell은 빈 상태로 유지한다.

나중에 Day 3을 채우지 않는다.

이를 통해 **실제 행동과 Visual History를 동일하게 유지한다.**

---

## 14. Notification Strategy

리텐션에서 중요한 기능으로 정의한다.

### 기본 알림

```text
퇴근 전에 청소하기 🧹
오늘 목표를 완료했나요?

[ 완료 ]
```

### Optional Second Reminder

MVP 이후 테스트한다.

예시:

```text
21:00

오늘 목표가 아직 남아 있어요.
```

하루 최대 2회까지 허용한다.

---

## 15. Success Metrics

MVP 단계에서는 MAU보다 **행동 기반 Metric**을 우선한다.

### North Star 후보

**Weekly Goal Completion Rate**

```text
완료 횟수
────────────
예정된 목표 횟수
```

---

### Activation

Goal 생성 이후 **첫 24시간 안에 첫 완료 경험**.

```text
Goal Created
↓
First Check Completed
```

Activation Rate:

```text
First Check User
───────────────
Goal Created User
```

---

### Retention

측정:

- D1
- D7
- D14

Retention은 사이트 재방문이 아니라 **다시 완료 기록을 했는지**를 기준으로 본다.

예시:

```text
D7 Goal Completion Retention
```

---

### Engagement

주간 예정 횟수 대비 완료율.

예시:

```text
예정 5일
완료 4일

Completion Rate = 80%
```

---

## 16. MVP Validation Criteria

2주 Prototype Test 기준.

예시 사용자 수:

```text
20명
```

Positive Signal:

- Goal 생성 → 첫 완료율 ≥ 70%
- D7 완료 기록 Retention ≥ 40%
- 알림 → 완료 Conversion ≥ 30%
- 7일 동안 목표를 3회 이상 기록한 사용자 ≥ 50%

위 수치는 업계 Benchmark가 아니라 초기 제품 검증을 위한 내부 기준으로 사용한다.

---

## 17. Out of Scope

MVP에서는 다음 기능을 제외한다.

- 여러 Goal
- 친구 기능
- Ranking
- Social Feed
- AI 추천
- 상세 통계
- Streak
- Level
- Badge
- 목표 Template Marketplace
- Apple Watch
- iOS Widget
- Android Widget
- 목표별 커뮤니티

---

## 18. Prototype Strategy

### Phase 0 — Concept Prototype

목적:

> Visual Reward가 동기를 만드는지 검증

형태:

- Figma Prototype
- 간단한 모바일 웹

Flow:

```text
오늘 목표
↓
완료
↓
그림 변화
```

테스트 인원:

```text
5~8명
```

확인할 것:

- 그림을 채우는 의미를 바로 이해하는가?
- 다음 칸을 채우고 싶은가?
- 날짜 기반이라는 것을 이해하는가?

---

### Phase 1 — Functional MVP

형태:

**PWA 기반 Mobile Web**

선정 이유:

- 링크로 바로 접근 가능
- 별도 앱 설치 불필요
- 홈 화면 추가 가능
- Push Notification 활용 가능
- iOS / Android 동시 테스트 가능

첫 MVP 단계에서는 Native App을 만들지 않는다.

---

## 19. Core Product Loop

```text
Reminder
↓
Remember Goal
↓
Do Action
↓
Check
↓
Visual Progress
↓
Small Reward
↓
Come Back Tomorrow
```

이 Loop가 실제로 반복되는지를 확인하는 것이 MVP의 핵심 목적이다.

---

## 20. Product Positioning

### 기존 Habit Tracker

> 습관을 기록하는 서비스

### 제안 Positioning

> 매일의 행동으로 하나의 그림을 완성하는 목표 달성 서비스

또는

> Complete a little every day.

제품은 `Calendar → Check → Statistics` 구조보다 아래 구조를 중심으로 설계한다.

```text
Goal
↓
Action
↓
Visual Reward
```

이 구조를 제품의 핵심 차별점으로 유지한다.
