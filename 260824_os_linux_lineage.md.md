# Unix, Linux, Ubuntu, CentOS의 차이와 관계

Unix, Linux, Ubuntu, CentOS는 모두 운영체제와 관련된 용어지만 각각 의미와 범위가 다르다.

---

## 1. 핵심 개념

| 용어 | 구분 | 설명 |
|---|---|---|
| **Unix** | 운영체제 계열 | 1969년 AT&T 벨 연구소에서 시작된 운영체제 |
| **Linux** | 커널 | Unix와 유사하게 동작하도록 독립적으로 개발된 오픈소스 커널 |
| **Ubuntu** | Linux 배포판 | Debian을 기반으로 제작된 범용 Linux 배포판 |
| **CentOS Linux** | Linux 배포판 | 과거 RHEL과의 호환성을 목표로 제공됐던 무료 배포판 |
| **CentOS Stream** | Linux 배포판 | 차기 RHEL 업데이트를 미리 개발하고 검증하는 배포판 |

---

## 2. Unix

**Unix**는 1969년 AT&T 벨 연구소에서 개발이 시작된 운영체제이다.

다중 사용자와 다중 작업 환경을 지원하도록 설계됐으며, 현대 운영체제의 구조와 명령어 체계에 큰 영향을 주었다.

### 주요 특징

- 다중 사용자 환경 지원
- 다중 작업 처리 지원
- 파일 중심의 시스템 구조
- 명령어 기반의 운영 환경
- 서버와 워크스테이션에서 주로 활용

### Unix 및 Unix 계열 운영체제

- AIX
- Solaris
- HP-UX
- BSD 계열
- macOS

> 상용 Unix는 소스 코드가 비공개이거나 라이선스 비용이 발생할 수 있지만, 모든 Unix 계열 운영체제가 폐쇄형인 것은 아니다.

---

## 3. Linux

**Linux**는 1991년 리누스 토르발스가 처음 공개한 오픈소스 운영체제 커널이다.

Unix의 소스 코드를 직접 가져온 것이 아니라, Unix와 유사한 구조와 사용 방식을 갖도록 독립적으로 개발되었다. 따라서 Linux는 일반적으로 **Unix-like 운영체제**로 분류된다.

### Linux 커널의 역할

- CPU 및 메모리 관리
- 프로세스 관리
- 파일 시스템 관리
- 장치 및 드라이버 관리
- 네트워크 통신 관리
- 하드웨어와 응용 프로그램 연결

> 정확히 말하면 Linux는 운영체제 전체가 아니라 운영체제의 핵심인 **커널**이다.

---

## 4. Linux 배포판

Linux 커널만으로는 일반 사용자가 완전한 운영체제로 사용하기 어렵다.

Linux 커널에 셸, 명령어, 라이브러리, 패키지 관리자, 서비스 관리 도구 등을 결합한 운영체제를 **Linux 배포판(Distribution)**이라고 한다.

### 대표적인 구성요소

```text
Linux 배포판
├── Linux Kernel
├── Shell
├── System Library
├── System Utilities
├── Package Manager
└── Service Manager
```

### 대표적인 배포판 계열

```text
Linux
├── Debian 계열
│   ├── Debian
│   └── Ubuntu
│
└── Red Hat 계열
    ├── Fedora
    ├── CentOS Stream
    ├── RHEL
    ├── Rocky Linux
    └── AlmaLinux
```

---

## 5. Ubuntu

**Ubuntu**는 Debian을 기반으로 만들어진 Linux 배포판이다.

Canonical에서 개발 및 지원하며, 데스크톱·서버·클라우드 등 다양한 환경에서 사용된다.

### 주요 특징

- Debian 계열
- `.deb` 패키지 형식 사용
- `apt` 패키지 관리자 사용
- AppArmor 보안 모듈 사용
- 일반 버전과 LTS 버전 제공
- 데스크톱과 서버 환경 모두 지원

```bash
sudo apt update
sudo apt install nginx
```

---

## 6. CentOS

### CentOS Linux

과거의 **CentOS Linux**는 RHEL의 공개 소스 코드를 기반으로 제작된 무료 Linux 배포판이었다.

RHEL과 높은 호환성을 제공하면서 무료로 사용할 수 있어 기업 서버와 교육 환경에서 널리 사용됐다.

하지만 CentOS Linux 7은 **2024년 6월 30일부로 지원이 종료**됐다.

### CentOS Stream

현재 CentOS 프로젝트는 **CentOS Stream**을 중심으로 운영된다.

CentOS Stream은 기존 CentOS Linux와 달리, 차기 RHEL 업데이트에 들어갈 기능을 먼저 반영하고 검증하는 역할을 한다.

```text
Fedora
  ↓
CentOS Stream
  ↓
RHEL
  ├── Rocky Linux
  └── AlmaLinux
```

### Red Hat 계열의 특징

- `.rpm` 패키지 형식 사용
- `dnf` 패키지 관리자 사용
- SELinux 보안 모듈 사용
- firewalld 방화벽 관리 도구 사용
- 기업 서버 환경에서 널리 활용

```bash
sudo dnf update
sudo dnf install nginx
```

> 과거에는 `yum`이 주로 사용됐지만, 현재 Red Hat 계열에서는 `dnf`가 기본 패키지 관리자로 사용된다.

---

## 7. Ubuntu와 CentOS 계열 비교

| 구분 | Ubuntu | CentOS Stream |
|---|---|---|
| 계열 | Debian 계열 | Red Hat 계열 |
| 패키지 형식 | `.deb` | `.rpm` |
| 패키지 관리자 | `apt` | `dnf` |
| 보안 모듈 | AppArmor | SELinux |
| 방화벽 도구 | UFW | firewalld |
| 개발 주체 | Canonical 및 커뮤니티 | CentOS Project 및 Red Hat 생태계 |
| 주요 성격 | 범용 Linux 배포판 | 차기 RHEL 업데이트 개발·검증 |
| 주요 환경 | 데스크톱, 서버, 클라우드 | RHEL 생태계 개발 및 테스트 |

---

## 8. 관계 정리

```text
Unix
  │
  └── 운영체제의 설계 철학과 구조에 영향
        │
        ▼
      Linux Kernel
        │
        ├── Debian ── Ubuntu
        │
        └── Red Hat 계열
              ├── Fedora
              ├── CentOS Stream
              ├── RHEL
              ├── Rocky Linux
              └── AlmaLinux
```

Linux는 Unix의 소스 코드를 직접 물려받은 운영체제가 아니다. Unix의 설계 철학과 인터페이스를 참고해 독립적으로 개발된 Unix-like 커널이다.

Ubuntu와 CentOS는 Linux 자체가 아니라, Linux 커널에 여러 프로그램과 관리 도구를 결합해 만든 배포판이다.

---

## 9. 최종 정리

- **Unix**는 현대 운영체제에 큰 영향을 준 운영체제 계열이다.
- **Linux**는 Unix와 유사하게 동작하도록 독립적으로 개발된 오픈소스 커널이다.
- **Ubuntu**는 Debian을 기반으로 만든 Linux 배포판이다.
- **CentOS Linux**는 과거 RHEL 호환 배포판이었지만 현재 지원이 종료됐다.
- **CentOS Stream**은 차기 RHEL 업데이트를 미리 개발하고 검증하는 배포판이다.
- Ubuntu와 CentOS Stream은 동일한 Linux 커널을 사용하지만 계열과 관리 도구가 다르다.