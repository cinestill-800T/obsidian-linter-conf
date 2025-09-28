# Obsidian Linter 設定

このディレクトリには、Obsidian Linter プラグイン用の設定ファイルが含まれています。

## ファイル

- `data.json` - Obsidian Linter の設定ファイル

## 設定概要

### YAML フロントマター設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `add-blank-line-after-yaml` | 有効 | YAML後に空行を追加 |
| `dedupe-yaml-array-values` | 有効 | YAML配列の重複値を除去 |
| `escape-yaml-special-characters` | 有効 | YAML特殊文字をエスケープ |
| `format-tags-in-yaml` | 有効 | YAMLタグの書式設定 |
| `format-yaml-array` | 有効 | YAML配列の書式設定（シングルライン） |
| `move-tags-to-yaml` | 有効 | インラインタグをYAMLに移動 |
| `sort-yaml-array-values` | 有効 | YAML配列の値をソート |
| `yaml-key-sort` | 有効 | YAMLキーをアルファベット順にソート |
| `yaml-timestamp` | 有効 | 作成・変更日時の自動挿入 |
| `yaml-title` | 有効 | ファイル名またはH1をタイトルとして設定 |

### 見出し設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `capitalize-headings` | 有効 | タイトルケースで見出しを整形 |
| `header-increment` | 有効 | H2から始まる見出し構造 |
| `headings-start-line` | 有効 | 見出しを行頭から開始 |
| `remove-trailing-punctuation-in-heading` | 有効 | 見出し末尾の句読点を除去 |

### フットノート設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `footnote-after-punctuation` | 有効 | 句読点後にフットノートを配置 |
| `move-footnotes-to-the-bottom` | 有効 | フットノートを文書末尾に移動 |
| `re-index-footnotes` | 有効 | フットノートの番号を再採番 |

### 書式設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `blockquote-style` | 有効 | 引用符後にスペース |
| `convert-bullet-list-markers` | 有効 | リストマーカーの統一 |
| `emphasis-style` | 有効 | 強調に `*` を使用 |
| `no-bare-urls` | 有効 | 裸のURLを禁止 |
| `ordered-list-style` | 有効 | 順序リストの書式統一 |
| `proper-ellipsis` | 有効 | 適切な省略記号の使用 |
| `strong-style` | 有効 | 太字に `**` を使用 |
| `unordered-list-style` | 有効 | リストマーカーに `-` を使用 |

### スペース・改行設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `compact-yaml` | 有効 | YAML のコンパクト化 |
| `consecutive-blank-lines` | 有効 | 連続する空行の除去 |
| `empty-line-around-blockquotes` | 有効 | 引用の前後に空行 |
| `empty-line-around-code-fences` | 有効 | コードブロックの前後に空行 |
| `empty-line-around-tables` | 有効 | テーブルの前後に空行 |
| `heading-blank-lines` | 有効 | 見出しの前後に空行 |
| `line-break-at-document-end` | 有効 | 文書末尾に改行 |
| `paragraph-blank-lines` | 有効 | 段落間に空行 |
| `space-after-list-markers` | 有効 | リストマーカー後にスペース |
| `trailing-spaces` | 有効 | 行末スペースの除去 |

### 日本語・中国語・韓国語特有の設定

| 機能 | 状態 | 説明 |
|------|------|------|
| `space-between-chinese-japanese-or-korean-and-english-or-numbers` | 有効 | CJK文字と英数字間のスペース自動挿入 |
| `remove-space-around-characters` | 有効 | 全角文字周りの不要なスペース除去 |
| `remove-space-before-or-after-characters` | 有効 | 特定文字の前後スペース調整 |

### ペースト時の設定

すべてのペースト時自動修正機能が有効化されています：

- 引用のインデント追加
- チェックリスト・リストアイテムの重複防止
- 省略記号の適切な変換
- ハイフンの除去
- 前後の空白除去
- 脚注の除去
- 複数空行の除去

## 特別な設定

### 無視設定

- **フォルダ**: `Templates`, `Attachments`
- **無視語句**: `macOS`, `iOS`, `iPhone`, `iPad`, `JavaScript`, `TypeScript`, `AppleScript`, `I`

### タイムスタンプ設定

- **形式**: `YYYY-MM-DD HH:mm:ss`
- **作成日**: ファイルシステムから取得
- **変更日**: ファイルシステムから取得
- **UTCへの変換**: 無効

### 大文字小文字の設定

- **小文字語句**: `a`, `an`, `the`, `of`, `to`, `in`, `on`, `for`, `and`, `or`, `nor`, `but`, `as`, `at`, `by`, `from`, `with`, `without`, `into`, `onto`

## 使用方法

### 1. インストール

1. Obsidianで「Linter」プラグインをインストール
2. プラグインを有効化

### 2. 設定の適用

1. Obsidianの設定を開く
2. Community plugins → Linter → 設定を開く
3. 「Import/Export Settings」から `data.json` をインポート

### 3. 使用

- **保存時自動実行**: `lintOnSave: true`
- **ファイル変更時実行**: `lintOnFileChange: true`
- **手動実行**: コマンドパレットから「Lint file」を実行

## 注意事項

- このプラグインはマークダウンファイルを自動的に修正します
- 重要なファイルは事前にバックアップを取ることをお勧めします
- 設定変更後はObsidianの再起動を推奨します

## カスタマイズ

設定をカスタマイズする場合は：

1. Obsidian内でLinter設定を変更
2. 「Export Settings」で新しい設定をエクスポート
3. `data.json` を更新

## 要件

- Obsidian
- Linter プラグイン（Community Plugin）
