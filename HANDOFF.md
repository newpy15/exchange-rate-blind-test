# 인수인계 문서 (AI A → AI B)

## 1. 목표
T04 검증 대시보드를 기반으로 실패→복구 시나리오가 정상 동작하는지 검증하고, 인수인계 절차를 문서화합니다.
남은 기능: 3계층 대조 검증 로직 보완 및 시나리오 로그 기록

## 2. 현재 상태
- 저장소 버전 ID: cd0e22cfc05698693b8b061bbf9a434741fd52ac
- index.html: 완성된 상태 (T04 대시보드)
- 테스트 환경: 브라우저에서 직접 실행 가능
- 7일 데이터 초기화/실패/복구 흐름 구현 완료
- 3계층 대조(T04-C10) 구현 완료

## 3. 실행 명령
```bash
# 브라우저에서 열기
start "" "C:\Users\User\Desktop\과제\t05\index.html"
# 또는 크롬으로 열기
"C:\Program Files\Google\Chrome\Application\chrome.exe" "C:\Users\User\Desktop\과제\t05\index.html"
```

## 4. 통과 검사 (고정 10개)
T05-CHK-01 ~ T05-CHK-10 - T05-CHECKS.json 참조
모든 검사 항목은 기존과 동일하게 유지해야 함 (삭제/완화/기대값 변경 금지)

## 5. 남은 문제
- console.log를 통한 A→인계→B 시작→B 완료 순서 로깅 추가 권장
- 스크린샷 캡처 (초기화→실패→복구)
- 테스트 결과 문서화

## 6. 다음 행동
1. 저장소 상태 확인 (git log 확인)
2. T05-CHECKS.json의 10개 검사 실행
3. 3계층 대조 섹션 확인 (모든 항목 일치 여부)
4. 실패 시나리오 재현: 실패 적용 → stale 상태 확인 → 복구 실행
5. 모든 검사 통과 확인 후 B 작업 완료 기록

## 7. 건드리지 말 것
- 기존 검증 로직의 핵심 함수 (normalizeNum, verifyTriple, makeRawLayer 등) 구조 변경 금지
- 고정 검사 10개(T05-CHK-01~10)의 ID/입력/기대값 변경 금지
- 7일 데이터 구조 (weekData) 기본 형식 변경 금지
- index.html의 UI 레이아웃 대폭 변경 금지

## 버전 정보
- 작업 폴더: C:\Users\User\Desktop\과제\t05
- Git 커밋: cd0e22cfc05698693b8b061bbf9a434741fd52ac
- AI A: Claude Sonnet
- AI B: GPT-4o (다른 서비스)
