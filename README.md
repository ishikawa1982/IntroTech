# やさしい技術解説シリーズ

MCP・CI/CD・WebSocket・Flyway・Getdown・Angular・BIG-IP・Spring・Docker・Kubernetes・NoSQL を、
たとえ話・図解・クイズでたどるやさしい解説サイトです。

## 見る

`index.html` をブラウザで開いてください。外部依存は Google Fonts のみで、
それ以外はすべて単体のHTML/CSS/JSで完結しています（ビルド不要）。

GitHub Pages で公開する場合は、リポジトリの Settings → Pages で
「Deploy from a branch」→ ブランチ `main` / フォルダ `/ (root)` を選ぶだけで動きます。

## 構成

```
index.html        トップページ（更新情報＋一覧＋横断用語索引）
mcp.html / cicd.html / websocket.html / flyway.html / getdown.html
angular.html / bigip.html / spring.html / docker.html / kubernetes.html
nosql.html
assets/site.css   全ページ共通のスタイル
```

## ページを増やすとき

1. 既存の解説ページ（例: `docker.html`）を複製し、`<link rel="stylesheet" href="assets/site.css">` はそのまま使う。
2. `index.html` 内の `PAGES` 配列に1エントリ追加する（ファイル名・タイトル・ひとこと説明）。
3. 同じく `TERMS` 配列に、そのページの用語を追加する（`read` にひらがな読みを入れると索引が正しい位置に並ぶ）。
4. 既存ページ末尾の `<section class="sibling">` に、新しいページへのリンクを足す（相互リンク）。
5. `index.html` 内の `NEWS` 配列の先頭に1行追加する（日付・見出し・本文）。トップページの「更新情報」に新しい順で並びます。
6. フッターの説明文の下に `<p class="footmeta">最終更新日: YYYY.M.D ｜ 参考文献: <a href="...">...</a></p>` を必ず追加する。最終更新日はページを作成・更新した日、参考文献はそのページを書くときに実際に参照した公式ドキュメントなどのリンクを記載する。

## ライセンス・免責

各ページの内容は学習用の平易な解説であり、各技術・製品の正式なドキュメントの代わりにはなりません。
バージョン依存の細部は、必要に応じて公式ドキュメントを参照してください。
