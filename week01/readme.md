# 2주차 실습: 서버 환경 구축 및 Docker 최적화

- **실습 일시**: 2026-01-13
- **작성자**: 20261234 홍길동

## 1. 실습 목표
- Ubuntu 24.04 환경에서 Docker 설치 및 nftables 충돌 해결
- AppArmor 프로필 적용을 통한 컨테이너 권한 제어

## 2. 주요 실행 명령어
- `sudo apt install docker.io`: Ubuntu 저장소 버전 Docker 설치
- `sudo nft list ruleset`: nftables 규칙 확인
- `sudo apparmor_parser -r`: AppArmor 프로필 적용

## 3. 트러블슈팅 기록
- **문제**: 컨테이너 내부 `/tmp` 폴더 쓰기 시 `Permission denied` 발생
- [cite_start]**원인**: AppArmor에서 `deny /tmp/** w` 정책 강제 적용 
- **해결**: 프로필 수정 후 재부팅 없이 정책 재로드하여 해결 확인

## 4. 실습 결과 (로그파일, 스크린샷 등)
[실습 로그 확인](./2026_홍길동_week01_log.txt)
[실습 화면 저장](./screen_week01 폴더)
