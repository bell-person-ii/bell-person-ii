# Lee Jong In

Spring Boot를 주로 사용해 백엔드를 개발합니다. 서비스 배포와 모니터링도 함께 맡고 있습니다.
RAG와 프롬프트 설계를 통해 LLM을 서비스에 활용하는 데 관심이 있습니다.

## Tech Stack

- **Backend**: Java, Spring Boot, Spring AI, TypeScript, Node.js(Express)
- **Database**: PostgreSQL(pgvector), Redis
- **Frontend**: Next.js, React
- **DevOps**: Docker, GitHub Actions, Nginx, Prometheus, Grafana

## Projects

### SSCC 운영관리시스템

숭실대학교 컴퓨팅 동아리의 업무, 회원, 학술 활동과 행사를 관리하는 서비스입니다. (2026.08 ~ 현재)<br>
[Server](https://github.com/SoongSilComputingClub/ssccops-server) · [Web](https://github.com/SoongSilComputingClub/ssccops-web)<br>
`Spring Boot` `Spring AI` `PostgreSQL` `pgvector` `Next.js` `GitHub Actions`

**담당 역할**: 백엔드 개발을 중심으로 회의, 업무, 하위업무 도메인과 학술 프로그램을 맡았습니다. 학술 프로그램 화면, 규정 도우미(RAG), 배포 자동화도 개발했습니다.

- 동아리 운영 기능 중 회의, 업무, 하위업무 도메인의 백엔드를 개발했습니다.
- 학술 프로그램의 백엔드와 화면을 개발했습니다. 모집과 선발, 회차별 출석, 기획안 제출을 지원하고 프로그램의 종료, 재시작, 폐지 처리를 구현했습니다.
- 스터디장이 사용하는 학술 앱(LMS)을 Next.js 모노레포에 추가했습니다.
- 규정 도우미의 RAG 처리 과정을 설계하고 구현했습니다. 회칙 문서를 파싱하고 나눠 색인하는 워커, 답변의 인용 검증, SSE 응답 스트리밍을 구현하고, 골든셋으로 회귀 테스트를 구성했습니다.
- GitHub Actions에서 빌드한 이미지를 GHCR에 올리고 Coolify로 배포하도록 개발·운영 환경의 배포 과정을 구성했습니다.

### AutoDevLog

키워드를 입력하면 LLM이 트러블슈팅 글을 작성해 Velog에 올려주는 서비스입니다. (2024.06 ~ 2024.07, 3인 팀)<br>
[Repo](https://github.com/AutoDevLog/AutoDevLog-Server)<br>
`Spring Boot` `WebFlux` `OpenAI API` `Redis`

**담당 역할**: 백엔드의 OpenAI API 연동과 글 생성 프롬프트 설계를 맡았습니다.

- 글 생성 기능에 OpenAI API를 연동했습니다.
- 문제(issue), 원인 추론(inference), 해결 방법(solution)의 세 단계로 글을 작성하도록 프롬프트를 설계했습니다.

### AgentBoard

Claude Code, Codex 같은 AI 코딩 에이전트의 사용량과 비용을 확인하는 대시보드입니다. (2026.06 ~ 현재)<br>
[Repo](https://github.com/hse09021/AgentBoard) · [Collector CLI](https://github.com/hse09021/agentboard-agent-collector)<br>
`TypeScript` `Express` `PostgreSQL` `Redis` `BullMQ` `Docker` `Prometheus`

**담당 역할**: 백엔드 개발과 배포 자동화, 운영 환경 개선을 맡고, 수집 CLI의 인증과 토큰 집계 기능을 개선했습니다.

- 백엔드를 모듈러 모놀리스 구조로 개발했습니다.
- GitHub Actions로 테스트, 버전 태그와 릴리스 생성을 자동화하고, 배포 후 헬스체크에 실패하면 자동으로 롤백하도록 했습니다.
- 공개 API에 캐시와 요청 제한을 적용하고 DB 인덱스를 최적화했습니다. Prometheus로 메트릭을, Loki로 로그를 수집하도록 구성했습니다.
- 수집 CLI에서 access token을 refresh token으로 자동 갱신하도록 하고, 에이전트별 토큰 사용량 집계의 정확도를 개선했습니다.

## Side Projects

- [ScrollToggle](https://github.com/bell-person-ii/ScrollToggle): 마우스 연결 여부에 따라 스크롤 방향을 자동으로 바꾸는 macOS 앱 (Swift)
- [n-seoul-tower-detector](https://github.com/bell-person-ii/n-seoul-tower-detector): YOLOv12-M을 파인튜닝해 이미지 속 N서울타워의 존재 여부와 위치를 찾는 객체 탐지 프로젝트 (Python)
- [Dorami_CG](https://github.com/bell-person-ii/Dorami_CG): OpenGL 기본 도형으로 도라미를 모델링하고 조명과 텍스처를 적용한 3D 뷰어 (C++)
- [jamak-ai](https://github.com/bell-person-ii/jamak-ai): Whisper와 NLLB로 영어 영상의 한글 자막을 자동 생성하는 로컬 웹앱
- [OpenUpScaler](https://github.com/bell-person-ii/OpenUpScaler): Real-ESRGAN으로 이미지 해상도를 높이는 로컬 앱
