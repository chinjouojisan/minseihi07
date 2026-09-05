# カコモと学ぶ 決算チャレンジ 民生費編 ― 公開用ファイル一式

## ファイル構成
```
index.html          本体(このファイルだけでも単独で動作します)
manifest.json        PWA設定(ホーム画面に追加した時のアプリ名・アイコン・色)
sw.js                Service Worker(ホーム画面追加を可能にする最小構成)
icon-192.png         PWAアイコン(小)
icon-512.png         PWAアイコン(大)
apple-touch-icon.png iPhoneのホーム画面用アイコン
og-image.png         SNSシェア時に表示されるカード画像(1200×630)
```

## 公開方法
1. この7ファイルを**同じフォルダに入れたまま**、まとめてサーバー(Google Pagesなど)にアップロードしてください。
2. `index.html`単体でも普通のWebページとして開けます。PWA機能(ホーム画面への追加)を使う場合は、他のファイルも同じ場所に置く必要があります。

## 公開前に直すところ
`index.html`の先頭付近(15〜16行目あたり)に、SNSシェア用の画像・URLを指定している箇所があります。

```html
<meta property="og:image" content="https://kakogawa-giin-map.com/kessan-challenge/minsei/og-image.png">
<meta property="og:url" content="https://kakogawa-giin-map.com/kessan-challenge/minsei/index.html">
```

実際に公開するURL(フォルダの場所)に合わせて、この2箇所を書き換えてください。書き換えないと、SNSでシェアした時の画像・リンクが正しく表示されません。

## 更新について
- 文言やちょっとした見た目の調整は、`index.html`をテキストエディタで直接編集すれば反映できます(単一ファイルなので、そのまま差し替えるだけでOKです)。
- クイズ問題・事業データ自体を追加・修正したい場合は、データ量が多く手作業では大変なので、次回もセッションを使って再生成することをおすすめします。

## 同梱している別ファイル
- `kessan_challenge_minsei_quiz77.txt`: クイズ全77問の問題・選択肢・正解一覧(テキスト形式、コピペ用)
