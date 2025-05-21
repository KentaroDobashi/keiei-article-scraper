# 経営メディア記事の自動収集スクリプト

## 📌 概要

指定した経営・ビジネス系カテゴリから、記事のURLを自動収集し、タイトルと本文をCSV形式で保存するPythonスクリプトです。

- 対象サイト：[https://keiei-manabu.com](https://keiei-manabu.com)
- 使用技術：Python（requests, BeautifulSoup, csv）
- 出力形式：CSV（URL / タイトル / 本文）

## 🔍 機能

- トップページから自動でカテゴリURLを抽出
- カテゴリ内の記事URLを再帰的に収集
- 各記事のタイトルと本文を抽出して整形
- 本文が短すぎる・空記事などは除外
- CSV形式で保存し、後続分析に活用可能

## ⚙️ カスタム設定・ノイズ除外

**対象外にしたページ（ノイズURL）は手動で厳選しています。**  
これは「本質的な情報収集」に集中するための設計です。

### ❌ 除外対象の例（人間の判断で排除）：
- プロフィールページ
- メルマガ登録やお問い合わせページ
- サイトマップやツール紹介
- 教材販売や一部の雑多カテゴリ

```python
exclude_urls = [
    "https://keiei-manabu.com/mailmagazinetouroku.html",
    "https://keiei-manabu.com/profile.html",
    "https://keiei-manabu.com/videoseminar",
    "https://keiei-manabu.com/toolkyouzai",
    ...
]
```
## 💡 応用アイデア（今後の展開）

- ChatGPT APIを使った自動要約・タグ分類
- 他サイトへの汎用化（クローラーツール化）
- 感情分析や話題抽出などのNLP処理
- 健康・旅・ライフログなど他分野への応用

