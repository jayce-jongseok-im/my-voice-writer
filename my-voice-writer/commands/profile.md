---
description: 내 글 샘플 프로필을 보거나 새로 저장합니다. (set / show / clear)
argument-hint: "set | show | clear"
---

내 문체 프로필을 관리합니다. 인자에 따라 다음 동작을 수행하세요.

**인자: `$ARGUMENTS`**

규칙:
- `show` (또는 빈 인자): `${CLAUDE_PLUGIN_DATA}/profile.md` 와 `${CLAUDE_PLUGIN_DATA}/style-notes.md` 의 내용을 읽어 요약해서 보여줍니다 (총 글자 수, 샘플 편 수, 마지막 200자 미리보기, 스타일 메모 전문). 파일이 없으면 "아직 프로필이 저장되지 않았습니다."라고 안내합니다.
- `set`: 사용자에게 새 글 샘플(2~4편, 합쳐서 800자 이상 권장)과 선택적인 스타일 메모를 요청합니다. 받은 내용으로 위 두 파일을 덮어씁니다. 디렉터리가 없으면 먼저 `mkdir -p ${CLAUDE_PLUGIN_DATA}` 를 실행합니다.
- `clear`: 사용자에게 정말 초기화할지 한 번 확인한 뒤, `${CLAUDE_PLUGIN_DATA}/profile.md` 와 `${CLAUDE_PLUGIN_DATA}/style-notes.md` 를 삭제합니다.

저장이나 삭제 후에는 결과를 한 줄로 한국어로 알려주세요.
