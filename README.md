# Charalette

Charaletteは、キャラクターを起点に衣装・プリセット・タグを自由に組み合わせ、画像生成用プロンプトを素早く作るWebアプリです。

> 管理ツールではなく、  
> **お気に入りだけを自由に組み合わせて遊べるパレット。**

「今日は、誰と遊ぶ？」から始めて、約2分で今日の一枚のためのPromptを組み立てることを目指します。

## Public App

- GitHub Pages: https://yoh-ret.github.io/Prompt_Palette/
- Browser title: `Charalette`
- Current Prototype: `Prompt_Palette_Prototype_v9_8.html`
- Current Master: `Prompt_Palette_Master_v10.xlsx`（883 tags / 18 categories / 113 Presets）

## Current MVP Features

- Local Character / Favorite / 並べ替え / 複製
- Character Thumbnail
- Characterなしモード
- Outfit Preset（作成・編集・複製・削除・Favorite）
- Preset Library / Tag Library
- Positive / Negative Prompt Preview・Copy
- 品質タグ ON / OFF・本文編集
- Backup / Restore
- iPhone Safariを主利用環境として実機受入済み

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

公開ブランドは **Charalette（キャラレット）** です。内部プロジェクト名および既存成果物識別子は互換性のため維持します。

- Repository: `yoh-ret/Prompt_Palette`
- Prototype filename: `Prompt_Palette_Prototype_vN_N.html`
- LocalStorage namespace: `promptPalette.v7_5.*`
- Backup format: `prompt-palette-backup`
- Backup schema version: `1`
- Backup filename: `Prompt_Palette_Backup_YYYY-MM-DD.json`

ブランド変更によるStorage migration、Master / JSONの改名、Backup schema変更は行いません。

## Source of Truth

設計・仕様・ログはGoogle Driveの内部プロジェクト **Prompt Palette** を正本とします。特に `README`、`INDEX`、`00_Project`、`20_WebApp`、`30_Data`、Development Log、Decision Logを優先します。

このリポジトリは、公開実装・Prototype履歴・変更履歴を管理します。

## Repository Structure

```text
Prompt_Palette/
├── README.md
├── index.html
└── prototype/
    └── Prompt_Palette_Prototype_v9_8.html
```

## Development Priorities

1. お気に入りだけを自由に組み合わせて遊べること
2. 約2分でPromptを完成できること
3. 既存仕様・既存データとの互換を保つこと
4. 創作の楽しさを邪魔する管理や設定を増やさないこと

## Public Release Readiness

LICENSE、favicon、OGP画像、独自ドメイン、repository名変更は未決定であり、今回の公開ブランド変更には含めていません。
