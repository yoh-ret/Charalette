# Charalette

Charaletteは、キャラクターを起点に衣装・プリセット・タグを自由に組み合わせ、画像生成用プロンプトを素早く作るWebアプリです。

> 管理ツールではなく、  
> **お気に入りだけを自由に組み合わせて遊べるパレット。**

「今日は、誰と遊ぶ？」から始めて、約2分で今日の一枚のためのPromptを組み立てることを目指します。

## Public App

- GitHub Pages: https://yoh-ret.github.io/Charalette/
- Repository: https://github.com/yoh-ret/Charalette
- Browser title: `Charalette`
- Current Prototype: `Prompt_Palette_Prototype_v10_2.html`
- Current Master: `Prompt_Palette_Master_v11.xlsx`（1138 tags / 18 categories / 142 Presets）
- Runtime Data: `prompt_palette_tags_v10.json` / `prompt_palette_categories_v10.json` / `prompt_palette_presets_v2.json`

## Current MVP Features

- Local Character / Favorite / 並べ替え / 複製
- Character Thumbnail
- Characterなしモード
- Outfit Preset（作成・編集・複製・削除・Favorite）
- Preset Library（6カテゴリ / Favorite / My / Builder選択モード） / Tag Library
- Positive / Negative Prompt Preview・Copy
- 品質タグ ON / OFF・本文編集
- Backup / Restore
- 既存機能はiPhone Safariで実機受入済み。v10.2追加Preset導線は実機確認待ち

## Prompt Generation Order

Positive Promptは、次の順で生成します。

1. Prompt Header / 品質タグ（OFF時は省略）
2. Character
3. Outfit
4. Preset / Tags

Negative PromptはCharacterとOutfitから別系統で生成・コピーします。

## Privacy and Data

Character、Outfit、My Preset、Favorite、品質タグ設定、Thumbnailは端末のLocalStorageに保存します。BackupはユーザーがJSONとして端末へ書き出し、Restoreは選択したファイルを端末内で読み込みます。

現行の公開HTMLには外部API、Analytics、tracking、外部フォント、外部画像、CDN、iframeは含まれていません。

## Compatibility

公開ブランドは **Charalette（キャラレット）** です。公開repositoryとGitHub Pages URLはCharaletteへ統一し、内部プロジェクト名および既存成果物識別子は互換性のため維持します。

- Repository: `yoh-ret/Charalette`
- Prototype filename: `Prompt_Palette_Prototype_vN_N.html`
- LocalStorage namespace: `promptPalette.v7_5.*`
- Backup format: `prompt-palette-backup`
- Backup schema version: `1`
- Backup filename: `Prompt_Palette_Backup_YYYY-MM-DD.json`

repository名変更によるStorage migration、Master / JSONの改名、Backup schema変更は行いません。

## Source of Truth

設計・仕様・ログはGoogle Driveの内部プロジェクト **Prompt Palette** を正本とします。特に `README`、`INDEX`、`00_Project`、`20_WebApp`、`30_Data`、Development Log、Decision Logを優先します。

このリポジトリは、公開実装・Prototype履歴・変更履歴を管理します。

## Repository Structure

```text
Charalette/
├── assets/
│   ├── charalette-logo.svg
│   ├── favicon.svg
│   ├── favicon-32.png
│   ├── favicon-48.png
│   ├── apple-touch-icon.png
│   ├── charalette-icon-512.png
│   └── og-charalette.png
├── README.md
├── index.html
└── prototype/
    ├── Prompt_Palette_Prototype_v10_0.html
    ├── Prompt_Palette_Prototype_v10_1.html
    └── Prompt_Palette_Prototype_v10_2.html
```

## Brand Assets

Charaletteの公開Brand Assetsは、Glass Lavender Themeとつながる手描きの `C + color dots` を共通シンボルとします。

- Wordmark: `assets/charalette-logo.svg`
- Favicon: SVG / 32×32 PNG / 48×48 PNG
- Apple Touch Icon: 180×180 PNG
- High-resolution icon: 512×512 PNG
- Open Graph image: `assets/og-charalette.png`（1200×630）

Top画面は受入済みのテキスト表示とHeroレイアウトを維持し、ロゴ画像への置換は行っていません。

## Development Priorities

1. お気に入りだけを自由に組み合わせて遊べること
2. 約2分でPromptを完成できること
3. 既存仕様・既存データとの互換を保つこと
4. 創作の楽しさを邪魔する管理や設定を増やさないこと

## Usage and Reuse

CharaletteはWebアプリとして公開しています。このGitHub repositoryは公開サイトのホスティングと公開実装・履歴管理のために利用しており、ソースコードや内部辞書・データを配布することを目的としていません。

LICENSEは設定していません。ソースコードおよび内部辞書・データの再利用・再配布・転載は、明示的な許可がある場合を除き認めていません。

## Public Release Readiness

favicon、Apple Touch Icon、OGP画像、canonical、Open Graph URLは新しいCharalette Pages URLへ反映済みです。repository名とPages URLのCharalette統一は完了しています。独自ドメインは現行MVPの公開には含めていません。
