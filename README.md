# METAUNIX | Claude × Fusion AI 3D 모델링 실습 가이드

## 현재 버전: v7 (2026-11-18)
기준: 사용자가 확정한 v5 HTML (`Fusion_AI_모델링_실습가이드_v5_문구수정.html`).

- 원본 섹션 여백·배경색·이미지·카피는 CSS 변환 없이 보존
- `landing.js`가 Shadow DOM 안에서 원본 CSS를 직접 로드하여 Sixshop 스타일과 충돌 방지
- 상단·하단 CTA 모두 실제 `<a href>`로 Monday.com 신청 폼 새 탭 연결 (JavaScript 이벤트에 의존하지 않음)
- `utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content` 전달
- 미리보기 '확대 보기' 표시 및 클릭 확대 기능 삭제
- 안내문: 가이드의 주요 화면을 미리 확인해 보세요. 상세 프롬프트와 실습 과정은 다운로드 자료에서 확인할 수 있습니다.

## Sixshop 적용 코드
```html
<link rel="stylesheet"
href="https://changgyupark.github.io/metaunix_claude-fusion/styles.css?v=20261118-03">

<script defer
src="https://changgyupark.github.io/metaunix_claude-fusion/landing.js?v=20261118-03"></script>
```

- 대상: `/claude-fusion` 페이지, Page ID `page2767890`
- 정상 동작 위해 GitHub Pages가 main/(root)로 게시되어야 함
- 기존 HEAD에서 **구 버전 스크립트는 삭제**하고 위 코드 한 세트만 남길 것
- GitHub Pages 게시 및 실제 랜딩/폼 제출 결과는 별도 실사이트 검증 필요

## 신청 폼
https://forms.monday.com/forms/af736c95d271f474447befa443f51450?r=apse2

## 테스트
상단 CTA / 하단 CTA 새 탭, 배경색/간격, 미리보기 4개 확대 없음, 모바일·데스크톱, UTM 5개, Monday 리드 및 메일 자동화, 경로 이탈 시 DOM 제거를 점검합니다.
