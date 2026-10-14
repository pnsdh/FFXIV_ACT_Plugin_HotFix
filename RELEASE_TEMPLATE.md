<!--
릴리스 설명 틀 (이 파일은 저장소용 메모 — 릴리스를 만들 때 아래 내용을 복사해 채운다)

태그 / 제목:  게임 패치 번호 (7.58, 핫픽스는 7.58h1)
첨부 파일:    FFXIV_ACT_Plugin_<패치>_custom_fix.7z
              ├ FFXIV_ACT_Plugin.dll                (ActPluginRepack 의 output\)
              ├ deucalion-x.y.z.distrib.dll         (output\ 에 있을 때)
              └ OverlayPlugin\opcodes.jsonc         (extras\OverlayPlugin\, 있을 때)
공식 업데이트가 나오면 이 릴리스는 지운다 (태그도: gh release delete <태그> --cleanup-tag).
-->

## <패치> 임시 패치본

> 공식 FFXIV_ACT_Plugin 업데이트 전까지 쓰는 비공식 임시본입니다. **FFLogs 업로드는 안 됩니다.**
> 공식 업데이트가 나오면 해루봇(또는 ACT)에서 업데이트하세요. 설치 방법은 [README](../../#직접-설치하기).

| | |
|---|---|
| 대상 게임 | 한국 `2026.xx.xx.0000.0000` / 글로벌 `2026.xx.xx.0000.0000` |
| 바탕 공식 플러그인 | `3.0.x.x` (deucalion `x.y.z`) |
| 만든 도구 | ActPluginRepack `2.x.x` |

### 바꾼 것

- opcode: <출처, 예: Yarukon CN_2026.xx.xx> — 한국/글로벌/중국 26개 중 <n>개 변경
- 패킷 후크: <예: Recv 시그니처 교체 (upstream deucalion main abc1234) / 변경 없음>
- 메모리 시그니처: <변경 없음 / 항목>
- 게임 데이터: <예: 한국어·영어 스킬/상태 이름 갱신>

### 확인한 것

- <예: sigcheck — 한국·글로벌 exe 에서 패킷 후크 모두 맞음>
- <예: opcode 출처끼리 대조 일치 (Yarukon = opcodediff = karashiiro)>
- <예: 실제 게임에서 데미지 미터 / 오버레이 동작 확인>

### 알려진 문제

- <없음 / 내용>
