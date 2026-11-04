> **這是翻譯。** 本檔是上游英文 README 的繁體中文（臺灣）譯文。程式碼、指令與連結都保持原樣。譯文若與原文不一致，以英文原文為準。上游日後若改了 README，這份譯文不會自動跟著更新。
>
> - 本儲存庫的英文原文：[README.md](README.md)
> - 本譯文所根據的上游版本 [`b5e8706`](https://github.com/ENZYME-APD/tapir-archicad-automation/commit/b5e8706d9de132982b4b3f9c5095dd277ffe3300)：[ENZYME-APD/tapir-archicad-automation 的 README.md](https://github.com/ENZYME-APD/tapir-archicad-automation/blob/b5e8706d9de132982b4b3f9c5095dd277ffe3300/README.md)
> - 上游原文最新版：[main 上的 README.md](https://github.com/ENZYME-APD/tapir-archicad-automation/blob/main/README.md)

# tapir-archicad-automation

[![Discord](https://img.shields.io/badge/Discord-join-blue?logo=discord&logoColor=fafafa)](https://discord.gg/NAnSennmpY)
[![Archicad Add-On Build Check](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/archicad_addon_build_check.yml/badge.svg)](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/archicad_addon_build_check.yml)
[![Grasshopper Plugin Build Check](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/grasshopper_plugin_build_check.yml/badge.svg)](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/grasshopper_plugin_build_check.yml)
[![Tapir Installer Build Check](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/installer_build_check.yml/badge.svg)](https://github.com/ENZYME-APD/tapir-archicad-automation/actions/workflows/installer_build_check.yml)
[![Archicad API coverage](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FENZYME-APD%2Ftapir-archicad-automation%2Fapi-coverage%2Fapi-coverage-badge.json)](https://enzyme-apd.github.io/tapir-archicad-automation/api-coverage/)
[![Grasshopper coverage](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FENZYME-APD%2Ftapir-archicad-automation%2Fapi-coverage%2Fgh-coverage-badge.json)](https://enzyme-apd.github.io/tapir-archicad-automation/gh-coverage/)

本儲存庫包含 Tapir Archicad 自動化套件，由下列元件組成：
- [Tapir Archicad 附加元件](archicad-addon)：在 Graphisoft 提供的官方指令之外，另外註冊多項新的 JSON 指令。新指令清單見[這裡](https://enzyme-apd.github.io/tapir-archicad-automation/archicad-addon)。已經可以使用，安裝方式請見下方說明。
- [Tapir Grasshopper 外掛](grasshopper-plugin)：讓不會寫程式的人也能使用上述元件的 Grasshopper 外掛。目前仍在開發中。

## Archicad API 涵蓋範圍

這裡顯示 Tapir 附加元件目前已經用到多少 Archicad API。圖會自動更新，每次變更後數分鐘內就會反映出來；[完整清單](https://enzyme-apd.github.io/tapir-archicad-automation/api-coverage/)列出每一個函式。若要申請其中一項，請開一則名為 "Archicad API request" 的 issue，並寫上該函式的名稱。

<a href="https://enzyme-apd.github.io/tapir-archicad-automation/api-coverage/">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ENZYME-APD/tapir-archicad-automation/api-coverage/api-coverage-dark.svg">
    <img alt="Tapir 的 Archicad API 涵蓋範圍" src="https://raw.githubusercontent.com/ENZYME-APD/tapir-archicad-automation/api-coverage/api-coverage.svg">
  </picture>
</a>

## Grasshopper 涵蓋範圍

這裡顯示 Grasshopper 外掛的元件呼叫了多少 Tapir 附加元件指令，以及是否涵蓋各指令的參數；更新方式與上一節相同。[完整清單](https://enzyme-apd.github.io/tapir-archicad-automation/gh-coverage/)列出每一項指令、對應的元件，以及尚未涵蓋的參數。

<a href="https://enzyme-apd.github.io/tapir-archicad-automation/gh-coverage/">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ENZYME-APD/tapir-archicad-automation/api-coverage/gh-coverage-dark.svg">
    <img alt="Tapir 指令的 Grasshopper 涵蓋範圍" src="https://raw.githubusercontent.com/ENZYME-APD/tapir-archicad-automation/api-coverage/gh-coverage.svg">
  </picture>
</a>

## 總覽

下圖說明這些元件以及彼此的相依關係。

![Tapir](branding/diagrams/TapirArchitecture.png?raw=true)

## 路線圖

[Tapir 路線圖在這裡。](https://github.com/orgs/ENZYME-APD/projects/4/views/1)

## 安裝

### Archicad 附加元件

#### 簡易安裝（建議）

下載並執行 Tapir 安裝程式。它會偵測已安裝的 Archicad 版本，下載相符的附加元件版本並安裝，因此下次啟動 Archicad 時會自動載入。

| Windows | macOS |
| --- | --- |
| [下載安裝程式](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirInstaller_Win.exe) | [下載安裝程式](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirInstaller_Mac.zip) |

注意事項：
- **Windows：** 安裝程式會要求系統管理員權限（它要把檔案複製到 Program Files 底下的 Archicad 資料夾）。由於這個執行檔沒有程式碼簽署，Windows SmartScreen 可能會警告發行者不明：請點選 "More info"，再點選 "Run anyway"。
- **macOS：** 將下載的檔案解壓縮後開啟 App（已簽署並完成公證）。

#### 手動安裝

請由此下載最新版本：

<!-- archicad-versions:start (written by tools/devkits.py update) -->
| Archicad 版本 | Windows | macOS |
| --- | --- | --- |
| Archicad 25 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC25_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC25_Mac.zip) |
| Archicad 26 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC26_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC26_Mac.zip) |
| Archicad 27 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC27_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC27_Mac.zip) |
| Archicad 28 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC28_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC28_Mac.zip) |
| Archicad 29 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC29_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC29_Mac.zip) |
| Archicad 30 | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC30_Win.apx) | [下載](https://github.com/ENZYME-APD/tapir-archicad-automation/releases/latest/download/TapirAddOn_AC30_Mac.zip) |
<!-- archicad-versions:end -->

下載附加元件檔案之後，還必須在 Archicad 裡安裝。請依照下列步驟安裝附加元件。

1. 將下載的檔案放在電腦上的某個位置。
2. 在 Archicad 中執行 "Options > Add-On Manager"。
3. 開啟 "Edit List of Available Add-Ons" 分頁，並點選 "Add"。
4. 瀏覽到已下載的附加元件檔案。
5. 在 Add-On Manager 中點選 "OK"。

### Grasshopper 外掛

可以從 Rhino Package Manager 安裝這個外掛。套件名稱是 "tapir"。

## 程式碼簽署政策

免費的程式碼簽署由 [SignPath.io](https://about.signpath.io) 提供，憑證由 [SignPath Foundation](https://signpath.org) 核發。

上述簽署適用於 Windows 安裝程式 `TapirInstaller_Win.exe`。它由 GitHub Actions 在 GitHub 裝載的執行器上，根據本儲存庫的原始碼建置，而且只有在手動核准之後才會簽署。若某個發行版本無法簽署，該版本的 Windows 安裝程式會以未簽署的形式發行，發行說明也會註明這一點。Windows 附加元件檔（`.apx`）沒有程式碼簽署。macOS 安裝程式與 macOS 附加元件則使用本專案自己的 Apple Developer ID 簽署並公證。

團隊角色：
- 提交者與審查者（Committers and reviewers）：擁有本儲存庫寫入權限的維護者。沒有寫入權限的人提出的拉取請求，以及本專案自動化從 issue 開立的草稿拉取請求，合併前都會由提交者審查，絕不會自動合併。安裝程式，以及建置與發行定義的變更，無論由誰提出，也都不會自動合併。
- 核准者（Approvers）：[Tibor Lorántfy](https://github.com/tlorantfy)

### 隱私

Tapir 安裝程式只會連線到 GitHub：
- 視窗開啟時，它會向 `api.github.com` 詢問最新的 Tapir 發行版本（若失敗，則改向 `github.com` 詢問）。
- 它會在您點選 Install 時，從 GitHub 的發行版本下載伺服器下載 Tapir 附加元件；若是您在 Archicad 中確認更新之後，由 Tapir 附加元件自己的更新程序啟動了安裝程式，也會自動下載。

這些都是一般的 HTTPS 請求。與任何網頁請求一樣，它們會向 GitHub 顯示您的 IP 位址與安裝程式名稱，並適用 [GitHub 一般隱私權聲明](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)。安裝程式不傳送個人資料、沒有遙測，也不會上傳任何內容。更新期間，它也會與您自己電腦上正在執行的 Archicad（127.0.0.1）通訊，以便關閉並重新啟動；附加元件會在更新前先告知這件事。此通訊不會離開您的電腦。安裝程式只會寫入您所選擇的那些 Archicad 安裝目錄中的 Add-Ons 資料夾；若是更新，則寫入正在更新的 Tapir 附加元件旁邊，另外會在暫存資料夾寫入暫存檔（更新鎖定檔 `TapirUpdate_<port>.lock` 會留在那裡）。它也可以再把附加元件移除（Uninstall 按鈕，或 `--uninstall`）。除此之外，除非使用者，或安裝、操作本程式的人明確要求，本程式不會將任何資訊傳輸到其他網路系統。

## 文件

- [Archicad JSON 指令](https://enzyme-apd.github.io/tapir-archicad-automation/archicad-addon)，每一項都附有 [archicad-addon/Examples](archicad-addon/Examples/) 的 Python 範例
- [工作流程](archicad-addon/Workflows/)：把多個指令組合成一項工作的 Python 腳本
- [Tapir GitHub wiki](https://github.com/ENZYME-APD/tapir-archicad-automation/wiki)
