# Prompt Palette

AI画像生成支援Webアプリ **Prompt Palette** の実装リポジトリです。

Prompt Paletteは、キャラクターごとの固定プロンプトを土台に、お気に入りのタグやプリセットを自由に組み合わせ、画像生成用プロンプトを素早く作ることを目的としています。

> 管理ツールではなく、  
> **お気に入りだけを自由に組み合わせて遊べるパレット**を目指します。

## Source of Truth

設計・仕様・辞書の正本は、Google Drive の `Prompt Palette` フォルダです。

特に以下を優先して参照します。

- `00_Project`
- `10_Dictionary`
- `20_WebApp`
- `30_Data`

このGitHubリポジトリは、実装コード・プロトタイプ・変更履歴を管理します。

## Current Status

- 開発フェーズ: MVP完成・実運用中
- 現行Prototype: v9.1
- 現行Master: v10（883タグ／18カテゴリ／113 Preset）
- 公開版: ルート `index.html`（GitHub Pages）
- 標準テーマ: Glass Lavender Theme

Prototype v9.1では、Character複製、Outfit Preset、Backup / Restore、Character並べ替えMVPを維持し、iPhone Safariでスクロール時にドラッグカードがずれる表示不具合を修正しています。

## Current MVP Stack

現行の正本では、MVPは以下の構成です。

- HTML
- CSS
- JavaScript
- JSON
- LocalStorage
- GitHub Pages

React / Firebase / Firestore への移行は、Architecture Map と Decision Log を更新したうえで検討します。

## Repository Structure

```text
Prompt_Palette/
├── README.md
├── index.html
└── prototype/
    └── Prompt_Palette_Prototype_v9_0.html
```

本実装へ進む段階で、正本に基づき以下の構成へ整理する予定です。

```text
Prompt_Palette/
├── index.html
├── style.css
├── app.js
├── components/
├── services/
├── data/
├── assets/
└── prototype/
```

## Prompt Generation Order

1. Prompt Header
2. Character Prompt
3. Preset
4. Tag
5. Negative Prompt

## Development Priorities

迷った場合は、以下を優先します。

1. お気に入りだけを自由に組み合わせて遊べること
2. 約2分でPromptを完成できること
3. 既存仕様との整合性
4. シンプルで拡張しやすいこと
5. 創作体験が楽しいこと

## Prototype

公開入口はルート `index.html`、正式保存版は `prototype/Prompt_Palette_Prototype_v9_0.html` です。
