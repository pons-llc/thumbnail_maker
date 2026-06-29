# サムネイルメーカー (Thumbnail Maker)

テキストを入力するだけで、文字だけのサムネイル画像を生成・ダウンロードできる完全フロントエンドのツールです。サーバー不要で、すべての描画はブラウザの Canvas API 上で行われます。

🔗 リポジトリ: https://github.com/pons-llc/thumbnail_maker.git
🌐 公開サイト: https://pons-llc.github.io/thumbnail_maker/

## 特徴

- テキストを入力するだけで文字ベースのサムネイルを作成
- デザインテーマがテンプレート化されている（classic / dark / blue）
- 入力項目はタイトル・サブタイトル・著者
- フォントサイズなどを調整可能
- PNG / JPG / WebP / SVG からダウンロード形式を選択可能
- 用途別の出力サイズプリセット（note / YouTube / OGP / wide / square / Twitter）

## 使い方

[index.html](index.html) をブラウザで開くだけで利用できます。

クエリパラメータで初期値を指定すると、自動でレンダリングされます。

```
index.html?title=AIが変える未来&subtitle=2025年の技術トレンド&author=山田花子&theme=dark&size=note
index.html?title=Weekly%20Report&author=Taro&theme=blue&size=ogp&titleSize=80
```

### クエリパラメータ

| パラメータ   | 説明                              | デフォルト | 値 / 範囲 |
|-------------|-----------------------------------|-----------|-----------|
| title       | メインタイトル（\n で改行）       | —         | 任意の文字列 |
| subtitle    | サブタイトル                      | —         | 任意の文字列 |
| author      | 著者名（右下に表示）              | —         | 任意の文字列 |
| theme       | カラーテーマ                      | classic   | classic, dark, blue |
| size        | 出力サイズ                        | note      | note, youtube, ogp, wide, square, twitter |
| titleSize   | タイトルのフォントサイズ (px)     | 96        | 24–120 |
| subSize     | サブタイトルのフォントサイズ (px) | 48        | 12–72 |
| authorSize  | 著者名のフォントサイズ (px)       | 24        | 10–48 |

### 出力サイズ

| ID       | サイズ        | 用途                     |
|----------|---------------|--------------------------|
| note     | 1280 × 670    | note.com の記事カバー    |
| youtube  | 1280 × 720    | YouTube サムネイル        |
| ogp      | 1200 × 630    | OGP / SNS カード          |
| wide     | 1280 × 512    | 5:2 ワイドバナー          |
| square   | 1080 × 1080   | Instagram スクエア        |
| twitter  | 1500 × 500    | Twitter ヘッダー          |

### テーマ

| ID      | 背景        | テキスト                |
|---------|-------------|-------------------------|
| classic | ホワイト    | 濃色テキスト + ブルー差し色 |
| dark    | ニアブラック | 白テキスト + ブルー差し色 |
| blue    | ディープブルー | 白テキスト              |

## ダウンロード

URL を開いた後、ページ上の **PNG / JPG / WebP / SVG** ボタンをクリックして画像を保存します。ファイル名には出力サイズ（例: `タイトル_ogp_1200x630.jpg`）が含まれます。

## 公開 (GitHub Pages)

このリポジトリは GitHub Pages で公開されています。`main` ブランチのルートにある [index.html](index.html) がそのまま配信されます。
