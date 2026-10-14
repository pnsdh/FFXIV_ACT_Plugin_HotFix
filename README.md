# FFXIV_ACT_Plugin HotFix

게임 패치 직후, **공식 FFXIV_ACT_Plugin 업데이트가 나오기 전까지** 잠깐 쓰는 임시 패치본입니다.

패치로 바뀐 부분(opcode, 패킷 후크 시그니처 등)만 갈아 끼운 플러그인을 [Releases](../../releases)에 올립니다.
공식 업데이트가 나오면 바로 공식본으로 돌아가세요.

> [!WARNING]
> - **공식 플러그인이 아닙니다.** [ravahn/FFXIV_ACT_Plugin](https://github.com/ravahn/FFXIV_ACT_Plugin) 의 공식 릴리스를
>   고친 비공식 임시본입니다. 이 패치본에서 생긴 문제를 공식 쪽에 신고하지 마세요.
> - **FFLogs 업로드는 안 됩니다.** 플러그인 버전 번호를 바꾸지 않고 원래 것을 그대로 쓰기 때문입니다.
> - 공식 업데이트가 나오면 해루봇(또는 ACT)에서 평소처럼 플러그인을 업데이트하세요. 이 패치본은 그걸로 정리됩니다.

## 받기

[Releases](../../releases)에서 **지금 게임 패치 번호**(예: `7.58`, 핫픽스는 `7.58h1`)의 릴리스를 받으세요.
릴리스 설명에 대상 게임 버전, 바탕이 된 공식 플러그인 버전, 바꾼 내용, 확인 결과가 적혀 있습니다.

공식 업데이트가 이미 나온 패치의 릴리스는 지웁니다 — 목록에 지금 패치가 없으면 공식본을 쓰면 됩니다.

## 더 쉬운 방법: ActPluginRepack

파일을 직접 넣는 게 번거롭다면 [ActPluginRepack](https://github.com/pnsdh/ActPluginRepack)을 쓰세요.
버튼 하나로 **고칠 필요가 있는지 확인 → 패치본 만들기 → ACT 에 설치**까지 해 주고, 원래 파일은 자동으로 백업해
[설치 전으로 되돌리기]로 돌아갈 수 있습니다. 이 저장소의 패치본도 같은 프로그램으로 만든 것입니다.

## 직접 설치하기

1. **ACT 와 게임을 끕니다.** (해루봇이 켜져 있으면 해루봇도)
2. **플러그인 폴더를 찾습니다.**
   - 해루봇: `<ACT 설치 폴더>\Plugins\FFXIV_ACT_Plugin_KR` (보통 `C:\Program Files (x86)\Advanced Combat Tracker\Plugins\FFXIV_ACT_Plugin_KR`)
   - 직접 설치한 ACT: ACT 의 Plugins 탭에서 FFXIV_ACT_Plugin.dll 이 있는 폴더
3. **원래 파일을 백업합니다.** 폴더의 `FFXIV_ACT_Plugin.dll` 과 `deucalion-*.dll` 을 다른 곳에 복사해 두세요.
4. **받은 파일을 넣습니다.**
   - `FFXIV_ACT_Plugin.dll` 을 덮어씁니다.
   - `deucalion-x.y.z.distrib.dll` 을 넣고, 폴더에 있던 **옛 `deucalion-*.dll` 은 지웁니다** (플러그인이 시작할 때
     `.distrib.dll` 을 정식 이름으로 바꿔 씁니다).
   - 압축 안에 `OverlayPlugin\opcodes.jsonc` 가 있으면 `<ACT>\Plugins\OverlayPlugin\resources\opcodes.jsonc` 를 바꿉니다
     (cactbot 등 오버레이용, 없으면 건너뜀).
5. **ACT 를 실행합니다.** 해루봇을 쓰면 해루봇에서 'ACT 실행'.

Program Files 안이라 파일을 바꿀 수 없으면 관리자 권한이 필요합니다. 백신(Windows Defender 등)이 deucalion 을 막으면
보호 기록에서 허용해 주세요 — 게임 메모리를 읽는 프로그램이라 오탐이 잦습니다.

### 해루봇을 쓸 때 알아 둘 것

- 해루봇의 플러그인 **업데이트 버튼을 누르면 공식본으로 덮어씁니다.** 공식 업데이트가 나온 뒤에만 누르세요.
- 해루봇은 켤 때마다 OverlayPlugin 의 `opcodes.jsonc` 를 원래 것으로 되돌립니다. 오버레이 일부가 안 맞으면 해루봇 대신
  ACT 를 직접 실행해 보세요. 데미지 미터 등 ACT 본체는 상관없습니다.

### 되돌리기

3번에서 백업한 파일을 다시 넣거나, 해루봇(또는 ACT)에서 FFXIV 플러그인을 다시 설치·업데이트하세요.

## 무엇을 바꾸나

소스를 다시 빌드하지 않고, 공식 플러그인 DLL 안의 리소스와 상수만 바꿉니다.

- **opcode** — 패치마다 바뀌는 패킷 번호 (Machina 의 지역별 opcode 표)
- **패킷 후크 시그니처** — 패치로 게임 코드가 바뀌어 deucalion 이 패킷을 못 잡게 됐을 때
- **메모리 시그니처** — 필요할 때만
- **게임 데이터** — 새 스킬·상태 이름 목록

각 릴리스 설명에 어느 출처의 값을 썼는지와 확인 결과를 적습니다. 바탕이 되는 공식 플러그인은 그 시점의 최신 공식
릴리스 그대로입니다.

## 고마운 곳

- [ravahn/FFXIV_ACT_Plugin](https://github.com/ravahn/FFXIV_ACT_Plugin) — 원본 플러그인 (Machina 포함)
- [ff14wed/deucalion](https://github.com/ff14wed/deucalion) — 패킷 후크
- [Yarukon/FFXIVNetworkOpcodes](https://github.com/Yarukon/FFXIVNetworkOpcodes), [xivdev/opcodediff](https://github.com/xivdev/opcodediff),
  [karashiiro/FFXIVOpcodes](https://github.com/karashiiro/FFXIVOpcodes) — opcode
- [OverlayPlugin](https://github.com/OverlayPlugin/OverlayPlugin) — opcodes.jsonc

플러그인과 각 구성 요소의 권리는 원래 저작자에게 있습니다. 문제가 있으면 이슈로 알려 주세요 — 바로 내리겠습니다.

---

**English** — Temporary hotfix builds of [FFXIV_ACT_Plugin](https://github.com/ravahn/FFXIV_ACT_Plugin) for the gap between a game
patch and the official plugin update. Only opcodes / hook signatures / game data are swapped inside the official release; the
plugin version is unchanged, so **FFLogs upload does not work**. Not official — do not report issues to ravahn. Switch back to
the official build as soon as it is released. Builds are made with [ActPluginRepack](https://github.com/pnsdh/ActPluginRepack),
which can also patch and install for you.
