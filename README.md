---
layout: page
title: SafeQR Legal Documentation Setup Guide
---

# SafeQR Legal Documentation

이 리포지토리는 SafeQR 앱의 법적 문서(개인정보처리방침 및 서비스 이용약관)를 포함하고 있습니다.

## GitHub Pages 설정 방법

이 문서들을 GitHub Pages로 게시하려면:

### 1. GitHub Pages 활성화
1. GitHub 리포지토리 설정으로 이동
2. "Pages" 섹션으로 이동
3. "Source"에서 "Deploy from a branch" 선택
4. `main` 또는 `master` 브랜치 선택
5. Root 폴더 `/` 선택
6. "Save" 클릭

### 2. 페이지 접근
몇 분 후, 다음 주소에서 페이지에 접근할 수 있습니다:
- **메인 페이지**: `https://[your-username].github.io/[repository-name]/`
- **개인정보처리방침**: `https://[your-username].github.io/[repository-name]/privacy-policy/`
- **서비스 이용약관**: `https://[your-username].github.io/[repository-name]/terms-of-service/`

### 3. 앱에서 링크 업데이트
앱의 설정에서 다음 링크를 사용하세요:
- 개인정보처리방침: `https://[your-username].github.io/[repository-name]/privacy-policy/`
- 서비스 이용약관: `https://[your-username].github.io/[repository-name]/terms-of-service/`

## 사용자화 필요사항

게시하기 전에 다음 사항들을 수정해주세요:

1. `_config.yml`에서 `url`을 실제 GitHub 사용자명으로 변경
2. `_config.yml`에서 `baseurl`을 실제 리포지토리 이름으로 변경
3. `[Your Company Address]`를 실제 회사 주소로 변경
4. `[Your Jurisdiction]`을 실제 관할 지역으로 변경
5. 이메일 주소가 다르다면 `privacy@sugaryple.com`과 `support@sugaryple.com` 업데이트

## 로컬 테스트

로컬에서 페이지를 테스트하려면:

```bash
# Jekyll 설치 (아직 설치하지 않은 경우)
gem install jekyll bundler

# 리포지토리 디렉토리로 이동
cd your-repository

# 의존성 설치
bundle install

# 로컬 서버 실행
bundle exec jekyll serve

# 브라우저에서 http://localhost:4000 방문
```

## 파일 구조

```
site/
├── _config.yml          # Jekyll 설정
├── index.md            # 법적 문서 링크가 있는 메인 페이지
├── privacy-policy.md   # 개인정보처리방침 (GDPR 준수)
├── terms-of-service.md # 서비스 이용약관
└── README.md          # 이 파일
```

## 유지보수

- 정책을 변경할 때마다 "최종 업데이트" 날짜를 업데이트하세요
- 정책 변경에 대한 버전 관리를 구현하는 것을 고려하세요
- 중요한 변경 사항은 인앱 알림을 통해 사용자에게 알리세요

## 규정 준수 참고사항

개인정보처리방침은 GDPR을 준수하도록 설계되었으며 다음을 포함합니다:
- 개인정보처리자의 명확한 식별
- 처리의 법적 근거
- 정보주체의 권리
- 국제 데이터 전송 조항
- 데이터 보존 기간
- 보안 조치

게시하기 전에 법무팀과 검토하시기 바랍니다.

## 도움말

문제가 발생하면:
1. GitHub Pages 설정이 올바른지 확인
2. `_config.yml`의 `url`과 `baseurl` 설정 확인
3. 파일명과 경로가 정확한지 확인
4. Jekyll 빌드 오류가 있는지 GitHub Actions 탭에서 확인

---

© 2025 Sugaryple. All rights reserved. 