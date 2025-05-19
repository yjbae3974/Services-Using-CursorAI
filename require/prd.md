📘 Project Overview
프로젝트명: AffinityAI
설명:
AI를 기반으로 사용자들의 관심사를 자동으로 분석하고, 유사한 관심사를 가진 사람들과 매칭시켜주는 소셜 네트워킹 앱입니다. 단순한 프로필 기반 매칭이 아닌, 사용자의 행동과 콘텐츠 소비 패턴을 AI가 학습하여 더 자연스럽고 유의미한 연결을 추구합니다.

🚀 Core Functionalities

1. 관심사 자동 분류 시스템
   사용자의 글, 검색, 좋아요, 태그 등을 기반으로 AI가 관심사를 자동 파악

카테고리는 동적으로 확장 가능 (예: "디지털노마드", "3D 프린팅", "인디 음악")

분류된 관심사에 따라 사용자 프로필 자동 생성

2. AI 기반 유저 매칭
   비슷한 관심사를 가진 사람들 간 매칭 추천

유사도 점수 기반으로 추천 우선순위 제공

사용자의 반응(채팅, 거절 등)에 따라 매칭 알고리즘 개선 (reinforcement-based)

3. AI 조언 시스템 (AI Match Assistant)
   첫 대화 주제, 공통 관심사 제안

매칭 상대에게 어떻게 말을 걸면 좋을지 자연어로 조언 제공

주기적 소셜 행동 리포트 제공 (예: "당신은 최근 3일간 5명과 대화를 시작했습니다!")

4. 프로필/피드 연동
   AI가 자동으로 프로필에 '관심사 태그' 삽입

사용자는 글이나 이미지를 올릴 수 있으며, AI가 이를 해석해 관심사로 반영

🛠️ Tech Stack & Technical Notes

1. 앱 개발
   구성 요소 기술
   클라이언트 앱 Flutter (iOS & Android 지원)
   상태관리 Riverpod / Bloc (선택 가능)
   UI Material Design 3 + Custom Theme
   실시간 기능 Firebase (Cloud Firestore + Realtime DB 활용 가능)

2. AI 기능 구현
   기능 기술 스택/모델
   관심사 분류 Sentence-BERT / OpenAI Embedding + KMeans
   유사도 매칭 Cosine Similarity + FAISS / Pinecone
   대화 조언 OpenAI GPT-4 / Claude / KoGPT 등 LLM 활용
   강화 학습 사용자 피드백 기반 간단한 점수 조정 로직 적용

3. 서버/백엔드
   Python (FastAPI or Firebase Functions)

데이터베이스: Supabase(PostgreSQL) 또는 Firebase Firestore

유저 인증: Firebase Auth

AI 파이프라인 배포: HuggingFace Spaces or custom cloud server (e.g., EC2)

4. 데이터 수집 및 처리
   사용자 피드/활동 로그 기반 분석

로그 데이터는 비식별화 처리하여 AI 학습에 활용

📚 참고 자료 및 필요 기술
OpenAI GPT API

Hugging Face Transformers & SentenceTransformers

FAISS for similarity search

Flutter 공식 문서

Firebase 문서: 인증, Firestore, Functions 등

AI 관심사 추출을 위한 오픈 데이터셋 (예: StackExchange, Reddit)

📁 Project Structure

```
lib/
├── core/
│   ├── constants/           # 앱 전체에서 사용되는 상수값들
│   ├── theme/              # 앱 테마 관련 설정
│   ├── utils/              # 유틸리티 함수들
│   └── widgets/            # 공통으로 사용되는 위젯들
│
├── features/
│   ├── auth/               # 인증 관련 기능
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   │
│   ├── profile/           # 프로필 관리 기능
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   │
│   ├── matching/          # AI 매칭 기능
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   │
│   ├── chat/              # 채팅 기능
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   │
│   └── ai_assistant/      # AI 조언 시스템
│       ├── data/
│       ├── domain/
│       └── presentation/
│
├── data/
│   ├── models/            # 데이터 모델 클래스들
│   ├── repositories/      # 데이터 저장소 구현체
│   └── datasources/       # 로컬/원격 데이터 소스
│
├── domain/
│   ├── entities/          # 비즈니스 엔티티
│   ├── repositories/      # 저장소 인터페이스
│   └── usecases/         # 비즈니스 로직 유스케이스
│
├── di/                    # 의존성 주입 설정
│
└── main.dart             # 앱 진입점

test/                      # 테스트 코드
├── unit/
├── widget/
└── integration/

assets/                    # 이미지, 폰트 등 리소스
├── images/
└── fonts/
```

각 feature 디렉토리 내부 구조:

```
feature/
├── data/
│   ├── datasources/      # 데이터 소스 구현
│   ├── models/           # 데이터 모델
│   └── repositories/     # 저장소 구현체
│
├── domain/
│   ├── entities/         # 비즈니스 엔티티
│   ├── repositories/     # 저장소 인터페이스
│   └── usecases/        # 유스케이스
│
└── presentation/
    ├── bloc/            # 상태 관리
    ├── pages/           # 화면
    └── widgets/         # 화면별 위젯
```

주요 특징:

1. Clean Architecture 패턴 적용
2. Feature-first 구조로 각 기능별 모듈화
3. 테스트 용이성을 고려한 구조
4. 확장 가능한 모듈식 설계
5. 의존성 주입을 통한 결합도 감소
