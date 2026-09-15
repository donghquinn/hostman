# hostman

[English](README.md) · [한국어](README.ko.md)

**hostman**은 HTTP, WebSocket, gRPC를 지원하는 빠르고 간결한 데스크톱
클라이언트입니다. 추적이나 클라우드 동기화 없이 로컬에서 즉시 실행됩니다.
이 저장소는 애플리케이션 소스가 아니라, 프로젝트의 공개 창구 —
소개 사이트와 다운로드 릴리스가 있는 곳입니다.

- 🔗 **사이트:** [donghquinn.github.io/hostman](https://donghquinn.github.io/hostman/)
- 💻 **애플리케이션 소스 및 문서:** [donghquinn/hostman-desktop](https://github.com/donghquinn/hostman-desktop)

---

## 이 저장소에 있는 것

| 파일 | 역할 |
|---|---|
| `index.html` / `index.ko.html` | 한 페이지짜리 소개 사이트, 영문/한글. `main` 브랜치에 push할 때마다 GitHub Pages로 자동 배포됩니다 (`.github/workflows/release.yml` 참고). |
| `hostman-logo.png` | 사이트 상단에 쓰이는 브랜드 로고. |
| `hostman-1.0.0.dmg` | 현재 macOS 릴리스 — 사이트의 설치 섹션에서 연결됩니다. |

Electron 셸, Go 백엔드, 프론트엔드, 그리고 실제 개발 문서는 모두
[hostman-desktop](https://github.com/donghquinn/hostman-desktop)에 있습니다.

## 다운로드

| 플랫폼 | |
|---|---|
| **macOS** | 유니버설 바이너리(Apple Silicon + Intel), 미서명 — [`hostman-1.0.0.dmg`](hostman-1.0.0.dmg), 약 198 MB. 공증을 받지 않아 처음 실행할 때 macOS 경고가 뜨는데, 이는 유료 애플 프로그램을 거치지 않은 모든 앱에 나타나는 현상일 뿐입니다. |
| **Windows / Linux** | hostman-desktop의 릴리스 파이프라인에서 빌드됩니다 — 해당 저장소의 [Releases](https://github.com/donghquinn/hostman-desktop/releases)를 확인하세요. |

Homebrew tap(`brew install --cask hostman`)은 준비 중이며 아직 배포되지
않았습니다 — 지금은 위 직접 다운로드를 이용해 주세요.

## hostman이 하는 일

세 가지 프로토콜을 하나의 창에서:

| | |
|---|---|
| **HTTP & REST** | JSON, Form Data, 바이너리 업로드를 포함한 GET, POST, PUT, DELETE, GraphQL. |
| **WebSocket** | 실시간 메시지, 라이브 피드, 이벤트 소켓을 위한 지속 연결. |
| **gRPC** | 코드 생성 없이 `.proto` 명세나 서버 리플렉션을 그대로 지원. |

계정도, 텔레메트리도, 유료 등급도 없습니다. 컬렉션은
`~/.hostman/collections/`에 읽을 수 있는 JSON으로 저장됩니다 — diff로 보고,
Git에 넣고, 파일 하나로 공유하세요.

## 의도적으로 제외한 기능

테스트 스크립트, 컬렉션 실행기, 목 서버·모니터링, 클라우드 팀 워크스페이스,
자동 OAuth 2.0 흐름, 영구 쿠키 저장소, 자동 요청 체이닝, 코드 생성기 —
모두 없습니다. 이런 기능이 필요한 워크플로라면 Postman이나 Bruno가 더 잘
맞을 것입니다. hostman의 범위는 일부러 좁게 잡았습니다.

## 사이트 개발하기

사이트는 별도 빌드 과정이 없는 순수 HTML/CSS입니다. `index.html` /
`index.ko.html`을 직접 수정해 `main`에 push하면 Pages 워크플로가 자동으로
배포합니다.

## 라이선스

MIT © 2026 Dong H. Kim — 전체 라이선스는
[hostman-desktop의 LICENSE](https://github.com/donghquinn/hostman-desktop/blob/main/LICENSE)를
참고하세요.
