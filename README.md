# ask releases

[ask](https://github.com/nextlevel-co/ask) のビルド済みバイナリ配布リポジトリです。ask は AI エージェントスキル（SKILL.md）の CLI パッケージマネージャーです。

## インストール

```bash
brew tap nextlevel-co/tap
brew install ask
```

## 使い方

```bash
ask init                                # プロジェクトに skills.json を作成
ask install hello                       # スキルをインストール
ask install hello@^1.0.0                # バージョン指定でインストール
ask install                             # skills.json の全スキルをインストール
ask uninstall hello                     # スキルを削除
ask update                              # スキルを最新互換バージョンに更新
ask list                                # インストール済みスキル一覧
ask list --outdated                     # 更新可能なスキルを表示
ask search <query>                      # レジストリからスキルを検索
ask info <name>                         # スキルの詳細情報
ask auth login --token <token>          # GitHub 認証
ask version                             # バージョン表示
```

### レジストリ指定

```bash
# 公式 Claude Code プラグインからインストール
ask install frontend-design --registry anthropics/claude-plugins-official

# カスタムレジストリからインストール
ask install hello --registry nextlevel-co/development-skills
```

### 対応ツール

- Claude Code
- Gemini CLI
- Codex
- カスタム

## 手動ダウンロード

[Releases](https://github.com/nextlevel-co/ask-releases/releases) ページからお使いのプラットフォーム向けバイナリをダウンロードしてください。

| プラットフォーム | ファイル |
|---|---|
| macOS (Apple Silicon) | `ask_*_darwin_arm64.tar.gz` |
| macOS (Intel) | `ask_*_darwin_amd64.tar.gz` |
| Linux (x86_64) | `ask_*_linux_amd64.tar.gz` |
| Linux (ARM64) | `ask_*_linux_arm64.tar.gz` |
| Windows (x86_64) | `ask_*_windows_amd64.tar.gz` |
| Windows (ARM64) | `ask_*_windows_arm64.tar.gz` |

## 検証

```bash
sha256sum -c ask_*_checksums.txt
```
