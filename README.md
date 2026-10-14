# FFXIV_ACT_Plugin HotFix

게임 패치 후 **공식 FFXIV_ACT_Plugin 업데이트가 나오기 전까지** 쓰는 임시 패치본입니다.

- 비공식입니다. 문제를 공식 플러그인 쪽에 신고하지 마세요.
- **FFLogs 업로드는 되지만, 클리어해도 랭킹에는 반영되지 않습니다.**
- 공식 업데이트가 나오면 해루봇(ACT)에서 업데이트해 공식본으로 돌아가세요.

## 받기

[Releases](../../releases)에서 지금 게임 패치 번호(예: `7.58`, `7.58h1`)를 받으세요.
목록에 없으면 공식본을 쓰면 됩니다.

## 설치

1. ACT·게임·해루봇을 끕니다.
2. 플러그인 폴더를 엽니다.
   해루봇: `C:\Program Files (x86)\Advanced Combat Tracker\Plugins\FFXIV_ACT_Plugin_KR`
3. 원래 파일을 다른 곳에 백업합니다.
4. 받은 zip 을 풀어 파일을 넣습니다.
   - `FFXIV_ACT_Plugin.dll` 덮어쓰기
   - `deucalion-*.distrib.dll` 넣고, 옛 `deucalion-*.dll` 은 지우기
   - `OverlayPlugin\opcodes.jsonc` 가 있으면 `Plugins\OverlayPlugin\resources\` 에 덮어쓰기
5. ACT 를 실행합니다.

되돌리려면 백업한 파일을 다시 넣거나, 해루봇에서 플러그인을 업데이트하세요.

> 해루봇의 **업데이트 버튼을 누르면 공식본으로 바뀝니다.** 공식 업데이트가 나온 뒤에 누르세요.

## 직접 패치하기

이 패치본은 [ActPluginRepack](https://github.com/pnsdh/ActPluginRepack)으로 만듭니다.
릴리스를 기다리지 않고 직접 패치해 쓸 수도 있습니다.

## 문의

[디스코드](https://discord.gg/R75tq68bA9)

## 사용한 프로젝트

[FFXIV_ACT_Plugin](https://github.com/ravahn/FFXIV_ACT_Plugin) ·
[deucalion](https://github.com/ff14wed/deucalion) ·
[FFXIVNetworkOpcodes](https://github.com/Yarukon/FFXIVNetworkOpcodes) ·
[opcodediff](https://github.com/xivdev/opcodediff) ·
[FFXIVOpcodes](https://github.com/karashiiro/FFXIVOpcodes) ·
[OverlayPlugin](https://github.com/OverlayPlugin/OverlayPlugin)

각 프로젝트의 권리는 원래 저작자에게 있습니다.
