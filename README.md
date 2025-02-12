
# まちがいさがしメーカー

間違い探しを誰でも「作成」「投稿」「シェア」「プレイ」できるWebアプリケーションです。<br>
正解画像と間違い画像を用意するだけで間違い探しが作成でき、他の人の投稿作品で遊ぶこともできます。<br>
レスポンシブ対応しているため、スマホからでも利用することができます。
![まちがいさがしメーカー](https://user-images.githubusercontent.com/75305753/122679072-5dd7a000-d224-11eb-92b6-5de9b6b55beb.gif)

|トップページ|プレイ画面|
|---|---|
|![](https://user-images.githubusercontent.com/75305753/120919307-d5211600-c6f3-11eb-89b3-efcdf7c40018.jpg)|![](https://user-images.githubusercontent.com/75305753/120919351-17e2ee00-c6f4-11eb-8cb0-2294a125e04f.jpg)|

# URL

~https://machigaesagashi.site~ <br>
※ [2024/02追記]　メンテナンスできていなかった為、一旦閉鎖しました 🙇 <br>
開発途中であるため、不具合等があるかもしれません。<br>
お気づきの際は[問い合わせフォーム](https://docs.google.com/forms/d/e/1FAIpQLSdHpcv83hmHh9XvRN5a35k-aEQ7UbGYJ93s5YDHQkUNkwERkw/viewform)等へ連絡頂けると幸いです。

# こだわりポイント

間違い探し投稿時に、間違い範囲を指定する際、面として塗りつぶして指定できるようにOpenCV.jsというライブラリを用いて実装しました。

<p align="center">
  <img src="https://user-images.githubusercontent.com/75305753/137131752-78411365-bc19-4674-93b2-42ca83e72dae.gif" />
</p>

# 使用技術
- Vue.js 2.6.12
- opencv.js
- Tailwind
- Firebase
  - Cloud Firestore
  - Firebase Hosting
  - Firebase Authentication(Twitter ログイン)
- GitHub Actions(CI/CD)
- Rollbar(エラーモニタリング)

# CI/CD

GitHub Actions を用いて以下のことを行っています。
- Pull Request の作成時にプレビューサイトをデプロイ
- Pull Request をマージ時に、本番サイトにデプロイ

# 機能一覧

- 間違い探しの投稿機能
  - 2枚の画像(正解画像と間違え画像)を投稿
  - 画像のトリミング(coropper.js)
  - 間違え位置の設定(opencv.js)
- Twitterシェア機能
- 検索機能
- 投稿作品で遊ぶ機能(pixijs)
- Twitterアカウントを用いたログイン機能
- 投稿作品の削除機能
- 動的OGP機能

# 今後実装予定の機能
- ゲームオーバーの概念の導入
- ライフ・時間制限の機能
- 連続タップへの制限

# 使用音源クレジット
- OtoLogic
