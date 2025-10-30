# study-timer-app
집중력 향상 타이머 앱 프로젝트
```mermaid
graph TD
    subgraph 1. 사용자 입력 및 실행 모듈
        A[타이머 UI / 입력 함수]
    end

    subgraph 2. 데이터 처리 및 관리 모듈
        B[데이터 저장/로드 함수]
    end

    subgraph 3. 분석 및 추천 모듈
        C[집중력 지수 산출 로직]
        D[최적 주기 추천 알고리즘]
    end

    subgraph 4. 보상 및 출력 모듈
        E[어항 게이미피케이션]
        F[학습 리포트 출력]
    end

    G[영구 데이터 저장소 (파일)]

    A --> B
    B -- StudySession, Interruption --> C
    C --> D
    D --> E
    D --> F
    B <--> G
    E -- RewardItem --> A
    F --> A
