# boxoffice — KOBIS 박스오피스 조회 스킬

## 하는 일
- 날짜(8자리, 예: 20261114)를 주고 "그날 박스오피스 1위가 뭐야?"라고 물으면 1위 영화 제목을 알려 줌
- 날짜와 영화 제목을 주고 "관객 수가 얼마야?"라고 물으면 그 영화의 일별 관객 수를 알려 줌

## 들어 있는 파일
- .claude/skills/boxoffice/SKILL.md
- .claude/skills/boxoffice/scripts/boxoffice.py
- .claude/skills/boxoffice/LICENSE

## 필요한 것
- tools.py, secret.py, 파이썬 패키지 requests

## 설치
- boxoffice 폴더를 .claude/skills/boxoffice/로 이동
- `/boxoffice` 를 입력

## 바깥으로 요청하는 곳
- https://www.kobis.or.kr/kobisopenapi/webservice/rest/boxoffice/searchDailyBoxOfficeList.json (영화진흥위원회 KOBIS 공식 API)
- 보내는 값은 API 키와 조회 날짜뿐임. 요청은 tools.py 가 보냄

## 키
- 자기 키를 secret.py에 넣을 것 

## 권한
- SKILL.md 에 allowed-tools 가 없음 -> 미리 허락된 도구가 없음
- 실행할 때마다 Claude Code 가 `python .claude/skills/boxoffice/scripts/boxoffice.py ...` 명령을 실행해도 되는지 물음

## 라이선스
- MIT License (저작권: 2026 최혜림)
