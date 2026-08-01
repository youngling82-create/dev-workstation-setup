# 개발 워크스테이션 구축 미션

## 프로젝트 개요

이 프로젝트는 개발 환경을 구축하고 필수 도구들을 설치하는 과정을 기록합니다.
- **목표**: 로컬 개발 환경 완성
- **주요 활동**: Git, Docker 설치 및 설정
- **최종 산출물**: GitHub 저장소 + 완성된 개발 환경

---

## 실행 환경

### 시스템 정보
- **OS**: macOS (Darwin Kernel 25.5.0)
- **Kernel Version**: 25.5.0 (Tue Jun 9 22:28:14 PDT 2026)
- **Architecture**: ARM64 (Apple Silicon T8140)
- **Hostname**: suaui-MacBook-Neo.local
- **Shell**: zsh

### 설치된 도구
| 도구 | 버전 | 상태 |
|------|------|------|
| Git | 2.50.1 (Apple Git-155) | ✅ 설치됨 |
| Docker | 29.4.0 (build 9d7ad9f) | ✅ 설치됨 |

---

## 프로젝트 구조
dev-workstation-setup/
├── README.md # 프로젝트 문서
├── app/ # 애플리케이션 파일
├── docs/ # 문서 저장소
├── logs/ # 로그 파일
└── screenshots/ # 스크린샷 저장소



---

## 체크리스트

- [x] GitHub Repository 생성 (youngling82-create/dev-workstation-setup)
- [x] 로컬 폴더 구조 생성
- [x] README.md 파일 생성
- [x] Git 초기화 및 첫 커밋
- [x] GitHub 연동 완료
- [x] 환경 정보 수집
- [ ] Docker 기본 설정 완료
- [ ] 개발 도구 추가 설정
- [ ] 최종 검증

---

## 검증 방법

### 1. 시스템 정보 확인
```bash
uname -a

git --version
git config --global user.email

docker --version
docker run hello-world

git status
git log --oneline

트러블슈팅
문제 1: Docker 실행 권한 오류
증상: permission denied while trying to connect to the Docker daemon

원인: Docker Desktop이 실행되지 않았거나 권한 설정 문제

해결방법:

Docker Desktop 애플리케이션 실행
터미널에서 다시 시도: docker run hello-world
여전히 오류 발생 시: sudo usermod -aG docker $USER
문제 2: Git 커밋 오류
증상: fatal: not a git repository

원인: 현재 디렉토리가 Git 저장소가 아님

해결방법:

프로젝트 폴더로 이동: cd ~/Desktop/dev-workstation-setup
Git 초기화: git init
원격 저장소 연동: git remote add origin https://github.com/youngling82-create/dev-workstation-setup.git
참고 자료
Git 공식 문서
Docker 공식 문서
macOS 개발 환경 설정
마지막 업데이트
작성일: 2025년
작성자: youngling82
상태: 진행 중