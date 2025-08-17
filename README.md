## 概要

- **目的**
  Markdown ノートを自動的に整形し、文書の可読性と一貫性を高めること。

- **特徴**
  - YAML メタデータの統一（配列整形、タグ移動、キーのソート、タイムスタンプ追加）
  - 見出し・段落のフォーマット統一（空行の付与、階層チェック）
  - 箇条書きや番号リストのスタイル統一
  - 太字・イタリック・省略記号・URL 表記などのルール固定
  - CJK（日本語・中国語・韓国語）と英数の間隔是正
  - ペースト時の書式乱れを自動修正
  - 保存時およびファイル変更時に自動整形

## 適用方法

1. Obsidian の **設定 → コミュニティプラグイン → Linter** をインストール。
2. 本リポジトリの `data.json` を以下の場所に配置：
   - macOS: `~/Library/Application Support/obsidian/YourVaultName/.obsidian/plugins/obsidian-linter/`
   - Windows: `%APPDATA%\Obsidian\YourVaultName\.obsidian\plugins\obsidian-linter\`
   - Linux: `~/.config/obsidian/YourVaultName/.obsidian/plugins/obsidian-linter/`
3. Obsidian を再起動、または Linter 設定画面でリロード。

## 主なルール

- **YAML**
  - `add-blank-line-after-yaml`
  - `yaml-key-sort`
  - `format-tags-in-yaml`
  - `move-tags-to-yaml`
  - `sort-yaml-array-values`
  - `yaml-timestamp`

- **見出し**
  - `capitalize-headings`
  - `headings-start-line`
  - `header-increment`
  - `remove-trailing-punctuation-in-heading`

- **リスト**
  - `convert-bullet-list-markers` → `-` に統一
  - `ordered-list-style` → 昇順番号 + `.` 終端
  - `unordered-list-style` → `-`

- **テキスト整形**
  - `emphasis-style` → `*`
  - `strong-style` → `**`
  - `no-bare-urls`
  - `proper-ellipsis`

- **スペーシング**
  - `trailing-spaces`
  - `consecutive-blank-lines`
  - `paragraph-blank-lines`
  - `empty-line-around-code-fences` / `tables` / `math-blocks` / `blockquotes`

- **ペースト時補正**
  - `prevent-double-checklist-indicator-on-paste`
  - `remove-hyphens-on-paste`
  - `remove-multiple-blank-lines-on-paste`
  - `proper-ellipsis-on-paste`

## 除外設定

- `Templates/` フォルダ
- `Attachments/` フォルダ

## 運用ポリシー

- **強制力を重視**した整形設定です。
  → 執筆スタイルのゆらぎを最小化し、ノートを一貫した形式で維持します。
- ルールが強すぎる場合は、必要に応じて `data.json` を編集してください。
