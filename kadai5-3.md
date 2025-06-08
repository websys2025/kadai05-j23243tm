## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
* エンドポイント：https://zipcloud.ibsnet.co.jp/api/search
このAPIは、日本の郵便番号を入力すると、それに対応する都道府県・市区町村・町域などの住所情報を返す機能を持つ。
* リクエストとレスポンスのフォーマット
* リクエスト形式例：
https://zipcloud.ibsnet.co.jp/api/search?zipcode=1000001
レスポンス形式（JSON）例：
{
  "message": null,
  "results": [
    {
      "address1": "東京都",
      "address2": "千代田区",
      "address3": "千代田",
      "kana1": "ﾄｳｷｮｳﾄ",
      "kana2": "ﾁﾖﾀﾞｸ",
      "kana3": "ﾁﾖﾀﾞ",
      "prefcode": "13",
      "zipcode": "1000001"
    }
  ],
  "status": 200
}
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
名称：Dog CEO’s Dog API
URL：https://dog.ceo/dog-api/
* エンドポイントと機能
* エンドポイント：https://dog.ceo/api/breeds/image/random
このAPIは、ランダムな犬の画像のURLを返す。ボタンを押すたびに異なる画像が取得できるため、視覚的に楽しめるAPIである。
* リクエストとレスポンスのフォーマット
* リクエスト形式（GET）例：
https://dog.ceo/api/breeds/image/random
レスポンス形式（JSON）例：
{
  "message": "https://images.dog.ceo/breeds/hound-basset/n02088238_11136.jpg",
  "status": "success"
}
### Q3-3. 感想
* 今回の課題で苦労したこと
* APIのレスポンスがJSON形式で返ってくるため、必要なデータをどのように取り出して表示するかを理解するのに時間がかかった。また、非同期処理の書き方やエラー処理の部分でもつまずいた。
* 演習を通して理解できたこと
* APIは、URLにリクエストを送信するだけで様々なデータを取得できる仕組みであることが分かった。また、JavaScriptを使ってそのデータをページに表示することで、動的なWebページが作れることを体験できた。
* Web APIの利便性や課題など
* Web APIは、天気、地図、画像など多くの外部データを簡単に取り込める点で非常に便利だと感じた。一方で、APIの提供側の仕様変更や通信エラーなどにより、常に安定して動くとは限らないという課題もあると感じた。
