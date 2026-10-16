# でんしゃ すごろく 首都圏版

首都圏の1,865駅を使った、スマートフォン向けのすごろくです。ひとり・CPU対戦・自動運転の「りょこう」に対応しています。

駅名を使った盤面をドラッグし、拡大・縮小して眺めながら遊べます。

## GitHub Pagesで公開

推奨リポジトリ名：`train-sugoroku-tokyo`

1. GitHubの新規リポジトリ作成画面で、Ownerを `Yamajet`、Repository nameを `train-sugoroku-tokyo`、公開範囲を **Public** にして作成します。
2. 解凍したフォルダーの**中身**をアップロードしてコミットします。`index.html` と `game.js` はリポジトリの直下に置きます。フォルダーごと入れ子にしないでください。
3. **Settings → Pages → Build and deployment** を開きます。
4. **Source: Deploy from a branch**、**Branch: main**、**Folder: /(root)** を選び、**Save** を押します。
5. Pages設定に表示される公開完了のURLから開きます。

設定完了後の想定URL：`https://yamajet.github.io/train-sugoroku-tokyo/`

ビルド・npm・サーバー側処理は不要です。初回の公開には少し時間がかかる場合があります。

## ファイル

- `index.html`：画面とスタイル
- `game.js`：ゲーム本体
- `network.json`：駅・路線の接続と読みデータ
- `credits.html`：データ出典・ライセンス

## 手元で動かす

Pythonが使える場合、このフォルダーで次を実行します。

```sh
python -m http.server 8000
```

ブラウザで `http://localhost:8000/` を開きます。首都圏版はファイルの直接ダブルクリックでは地図データを読み込めないため、上記のようなHTTPサーバーを使ってください。

## 更新

修正したファイルを同じ場所にアップロード、またはGitHub DesktopなどでコミットしてPushします。公開元ブランチの更新がGitHub Pagesに反映されます。

元の路線図PDFやデータの取得用CSV、認証情報、別サービス用の公開設定はこの配布物には含みません。
