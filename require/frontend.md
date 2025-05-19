# Project Overview (프로젝트 개요)

AffinityAI는 AI 기반 소셜 네트워킹 앱으로, 사용자의 관심사를 자동으로 분석하고 유사한 관심사를 가진 사람들과 매칭해주는 서비스입니다.

## Tech Stack

-   Framework: Flutter (iOS & Android)
-   State Management: Riverpod
-   UI Framework: Material Design 3 + Custom Theme
-   Real-time Features: Firebase (Cloud Firestore + Realtime DB)

# Feature Requirements (기능 요구사항)

## 1. 사용자 인증 및 프로필

### 1.1 인증 시스템

-   [ ] Firebase Authentication 연동
-   [ ] 소셜 로그인 (Google, Apple, Kakao)
-   [ ] 이메일/비밀번호 회원가입
-   [ ] 비밀번호 재설정
-   [ ] 자동 로그인 처리

### 1.2 프로필 관리

-   [ ] 기본 프로필 정보 입력/수정
-   [ ] AI 기반 관심사 태그 자동 생성
-   [ ] 프로필 이미지 업로드/수정
-   [ ] 관심사 태그 수동 추가/삭제
-   [ ] 프로필 공개 설정

## 2. AI 매칭 시스템

### 2.1 매칭 알고리즘 UI

-   [ ] 매칭 카드 스와이프 인터페이스
-   [ ] 매칭 상대 프로필 표시
-   [ ] 공통 관심사 하이라이트
-   [ ] 매칭 거절/수락 애니메이션
-   [ ] 매칭 히스토리 관리

### 2.2 AI 조언 시스템

-   [ ] 첫 대화 주제 추천 UI
-   [ ] 대화 시작 가이드 표시
-   [ ] 실시간 대화 조언
-   [ ] 소셜 행동 리포트 대시보드

## 3. 채팅 시스템

### 3.1 실시간 채팅

-   [ ] Firebase Realtime DB 연동
-   [ ] 메시지 전송/수신
-   [ ] 읽음 표시
-   [ ] 타이핑 인디케이터
-   [ ] 이미지/파일 공유

### 3.2 채팅 UI/UX

-   [ ] 채팅방 목록
-   [ ] 채팅방 상세
-   [ ] 메시지 버블 디자인
-   [ ] 스크롤 위치 관리
-   [ ] 새 메시지 알림

## 4. 피드 시스템

### 4.1 콘텐츠 관리

-   [ ] 게시물 작성/수정/삭제
-   [ ] 이미지/텍스트 포스팅
-   [ ] 좋아요/댓글 기능
-   [ ] AI 기반 콘텐츠 분석
-   [ ] 관심사 태그 자동 추출

### 4.2 피드 UI

-   [ ] 무한 스크롤
-   [ ] 게시물 카드 디자인
-   [ ] 이미지 갤러리
-   [ ] 상호작용 애니메이션
-   [ ] 콘텐츠 필터링

# Implementation Plan (구현 계획)

## Phase 1: 기본 인프라 구축 (2주)

-   [ ] 프로젝트 초기 설정
-   [ ] 디렉토리 구조 설정
-   [ ] 기본 테마 및 디자인 시스템 구축
-   [ ] Firebase 연동
-   [ ] 기본 네비게이션 구현

## Phase 2: 인증 및 프로필 (2주)

-   [ ] 인증 시스템 구현
-   [ ] 프로필 관리 기능
-   [ ] 이미지 업로드 시스템
-   [ ] 관심사 태그 시스템

## Phase 3: 매칭 시스템 (3주)

-   [ ] 매칭 알고리즘 UI 구현
-   [ ] AI 조언 시스템 연동
-   [ ] 매칭 히스토리 관리
-   [ ] 실시간 매칭 상태 업데이트

## Phase 4: 채팅 시스템 (2주)

-   [ ] 실시간 채팅 구현
-   [ ] 채팅 UI/UX 구현
-   [ ] 메시지 알림 시스템
-   [ ] 미디어 공유 기능

## Phase 5: 피드 시스템 (2주)

-   [ ] 피드 UI 구현
-   [ ] 게시물 CRUD 기능
-   [ ] 상호작용 기능
-   [ ] AI 기반 콘텐츠 분석 연동

## Phase 6: 최적화 및 테스트 (1주)

-   [ ] 성능 최적화
-   [ ] UI/UX 개선
-   [ ] 버그 수정
-   [ ] 사용자 테스트

# UI/UX Guidelines (UI/UX 가이드라인)

## Design System

-   Material Design 3 기반 커스텀 테마
-   일관된 색상 팔레트
-   타이포그래피 시스템
-   컴포넌트 라이브러리

## Responsive Design

-   다양한 화면 크기 대응
-   태블릿 레이아웃 지원
-   방향 전환 대응

## Accessibility

-   스크린 리더 지원
-   키보드 네비게이션
-   색상 대비 준수

# Testing Strategy (테스트 전략)

## Unit Tests

-   비즈니스 로직
-   유틸리티 함수
-   상태 관리

## Widget Tests

-   UI 컴포넌트
-   사용자 상호작용
-   애니메이션

## Integration Tests

-   화면 간 네비게이션
-   데이터 흐름
-   API 연동

# Performance Optimization (성능 최적화)

## Image Optimization

-   이미지 캐싱
-   레이지 로딩
-   적절한 이미지 포맷

## State Management

-   효율적인 상태 업데이트
-   불필요한 리빌드 방지
-   메모리 누수 방지

## Network Optimization

-   API 요청 최적화
-   데이터 캐싱
-   오프라인 지원

# Security Considerations (보안 고려사항)

## Data Protection

-   민감 정보 암호화
-   안전한 저장소 사용
-   세션 관리

## Authentication

-   토큰 관리
-   자동 로그아웃
-   보안 정책 적용

# Monitoring and Analytics (모니터링 및 분석)

## Error Tracking

-   크래시 리포트
-   에러 로깅
-   사용자 피드백

## Analytics

-   사용자 행동 추적
-   성능 메트릭
-   A/B 테스트

# Deployment Strategy (배포 전략)

## App Store

-   iOS 앱스토어 배포
-   Android 플레이스토어 배포
-   버전 관리

## CI/CD

-   자동화된 빌드
-   테스트 자동화
-   배포 파이프라인
