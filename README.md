# METAUNIX | Claude × Fusion AI 3D 모델링 실습 가이드

## 최종 작업 버전 v9 (2026-11-19)

기준: 최종 v5 HTML, Sixshop Page ID `page2767890`, 경로 `/claude-fusion`.
기존 디자인·배경·여백·이미지, 스크롤 등장 효과 및 UTM 연결을 유지한 수정본.

### 변경
- 미리보기 4개: 마우스 호버 시 이미지 위치에 따라 움직이는 원형 확대 렌즈(2.4배); 클릭 팝업 없음
- 터치 기기에서는 원본 이미지 그대로 노출
- 하단 `무료 실습 가이드 받기`는 상단과 동일한 실 링크로 연결
- CTA 클릭 시 새 탭으로 Monday WorkForm 오픈, 팝업 차단 시 현재 탭으로 이동하는 대체 처리
- UTM 5종 `utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content` 유지

### Sixshop HEAD (구 버전 코드 제거 후 적용)

```html
<link rel="stylesheet"
href="https://changgyupark.github.io/metaunix_claude-fusion/styles.css?v=20261119-02">

<script defer
src="https://changgyupark.github.io/metaunix_claude-fusion/landing.js?v=20261119-02"></script>
```

**반드시 이전 버전 script/link는 완전히 삭제하고 새 코드 한 세트만 사용.**
GitHub Pages는 해당 저장소 main/(root)에서 활성화되어야 함. 
정상 응답 및 실제 Sixshop 사이트 렌더링은 별도 실사이트 점검 필요.

### 필수 최종 QA
1. Hero를 포함한 모든 섹션 여백·배경 및 모바일 표시
2. 미리보기 이미지 4개 마우스 오버 돋보기(2.4배), 클릭 확대 없음
3. 상단과 **최하단** 무료 실습 가이드 버튼 모두 Monday 폼 새 탭 열기
4. UTM 5종과 Monday 리드 등록, 이메일 자동 발송
5. Sixshop 다른 페이지에서 랜딩 코드 미실행
