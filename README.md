# METAUNIX | Claude × Fusion AI 3D 모델링 실습 가이드

Sixshop 외부 JS 로딩용 소스입니다. v5 최종 HTML 디자인/카피/미리보기 이미지를 보존합니다.

- 실제 페이지: https://metaunix.co.kr/claude-fusion
- Sixshop Page ID: `page2767890`
- 원본 빈 섹션: `section17448718`
- Monday.com 신청 폼: https://forms.monday.com/forms/af736c95d271f474447befa443f51450?r=apse2
- 코드: `landing.js` (구조/인터랙션/CTA 및 UTM), `styles.css` (Shadow DOM 격리 스타일)

## Sixshop 공통 디자인 편집 애드온 <head> 등록 코드

```html
<script defer src="https://cdn.jsdelivr.net/gh/ChanggyuPark/metaunix_claude-fusion@main/landing.js"></script>
```

CSS는 JS가 Shadow DOM 내부로 동적 로드합니다. 기존 Sixshop Header/Footer는 유지됩니다.
JS는 경로가 정확히 `/claude-fusion`이고 `#page2767890`이 존재할 때만 작동합니다.
Sixshop SPA 페이지 전환에서도 활성화/복구를 점검합니다.

상단/하단 신청 CTA는 새 탭에서 동일한 WorkForm을 엽니다. 
랜딩 유입 URL의 `utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content`를 폼으로 전달합니다. 
세션 중 다른 페이지로 이동해도 가능한 경우 마지막 UTM을 기억합니다.

## 테스트 체크리스트

1. Sixshop 일반 페이지 콘텐츠 최소 문구 발행, HEAD 코드 적용
2. 데스크톱/모바일 페이지 로드 및 본문/미리보기/라이트박스 확인
3. 상단·하단 CTA 모두 새 탭에서 Monday WorkForm으로 이동 확인
4. 예: `https://metaunix.co.kr/claude-fusion?utm_source=meta&utm_medium=paid_social&utm_campaign=claude_fusion&utm_content=creative_01&utm_term=ai_modeling`
5. Monday WorkForm URL에 UTM 5종 존재 확인; 실제 제출 후 리드 컬럼 반영 검증
6. 기존 폼 자동발송 설정이 새 자료에도 대응하는지 점검

## 주의
GitHub 파일을 커밋했다고 Sixshop 사이트에 자동 표시되는 것은 아닙니다. 
Sixshop 공통 HEAD에 위 script를 등록해야 합니다. GitHub Pages 활성화 없이도 jsDelivr를 통해 로딩할 수 있습니다.
