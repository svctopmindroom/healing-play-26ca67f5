# 캐릭터 설명 문구 제거

## 요약
캐릭터 선택 화면에서 각 캐릭터 카드 아래에 표시되는 성격 설명 문구(`desc`)를 제거합니다.

## 현재 상태
- `src/components/CharacterSelect.tsx`의 `characters` 배열에 각 캐릭터가 `desc` 필드를 가지고 있습니다.
- 렌더링 시 `{char.desc}`를 출력하는 `<span>`이 카드 내부에 있습니다.

## 변경 내용
1. `characters` 배열에서 `desc` 필드를 삭제합니다.
2. 카드 내부의 `{char.desc}` 설명 `<span>`을 제거합니다.
3. 남은 콘텐츠(이모지, 레이블, 성격 태그)의 간격과 레이아웃이 자연스럽게 유지되도록 확인합니다.

## 영향 범위
- `src/components/CharacterSelect.tsx`만 수정합니다.
- `CharacterInfo` 인터페이스에는 `desc`가 없으므로 타입 변경은 없습니다.

## 검증
- 저장 후 TypeScript 빌드/컴파일 오류가 없는지 확인합니다.
- 미리보기에서 캐릭터 선택 화면의 4개 카드가 설명 문구 없이 정상 표시되는지 확인합니다.
