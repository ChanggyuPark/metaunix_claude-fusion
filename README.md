# METAUNIX Claude × Fusion AI 3D 모델링 실습 가이드

최종 원본: `Fusion_AI_모델링_실습가이드_v5_문구수정.html` (사용자가 제공한 최종 HTML).
그 원본을 보존하고 **상단·하단 CTA의 Monday.com 연결 및 UTM 5종 전달**만 추가한 v6입니다.

- 사용자 확인 Sixshop URL: https://metaunix.co.kr/claude-fusion
- Sixshop Page ID: `page2767890`
- placeholder section: `section17448718`
- Monday WorkForm: https://forms.monday.com/forms/af736c95d271f474447befa443f51450?r=apse2

## 파일
- `Fusion_AI_모델링_실습가이드_v6_폼연결.html`: 원본 비교·단독 미리보기용 HTML
- `landing.js`: Sixshop 경로·Page ID 이중 잠금, HTML 삽입, 미리보기 확대, CTA/UTM 5종 연결, SPA 전환 시 복구
- `styles.css`: CSS 선택자를 `#metaunix-claude-fusion-app` 아래로 격리

## Sixshop 공통 <head> 삽입

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ChanggyuPark/metaunix_claude-fusion@main/styles.css?v=2">
<script defer src="https://cdn.jsdelivr.net/gh/ChanggyuPark/metaunix_claude-fusion@main/landing.js?v=2"></script>
```

JS/CSS 두 파일을 각각 명시적으로 로드합니다. 기존 사이트 Header/Footer는 제거하거나 변경하지 않습니다.
`/claude-fusion`와 `#page2767890`가 모두 맞는 경우에만 랜딩을 렌더링합니다.

## 최종 테스트

1. HEAD 코드 적용 후 PC/모바일 레이아웃 및 사이트 Header/Footer 확인
2. 미리보기 4종 클릭 확대 및 닫기
3. 상단·하단 CTA가 새 탭에서 Monday 폼으로 열리는지
4. `?utm_source=meta&utm_medium=paid_social&utm_campaign=claude_fusion&utm_term=ai_modeling&utm_content=creative_01`로 접속 후 폼에 5개 전달되는지
5. 테스트 폼 제출, 보드 컬럼 및 자동 발송 확인
6. 브라우저 뒤로 가기/다른 페이지 이동 시 다른 페이지에 렌더되지 않는지 확인

주의: GitHub 커밋은 완료되어도 Sixshop의 HEAD 코드를 추가하기 전까지 사이트에는 표시되지 않습니다.
