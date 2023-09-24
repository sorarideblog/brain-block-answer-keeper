# brain-block-answer-keeper
[「永久に遊べるパズル 脳ブロック」（株式会社テンヨー）](https://toyhobby.tenyo.jp/bb/lineup.html)の紙の記録用紙の代替となるツール。

> **Warning**
> このツールは非公式です。株式会社テンヨーとは一切関係ありません。
> また、このツールの使用は自己責任でお願いします。いかなる損害が発生しても、作者は一切の責任を負いません。

> **Note**
> このツールは現在仕様検討および開発中です。まだ使用できません。

# 背景
「永久に遊べるパズル 脳ブロック」は公式から[記録用紙](https://bb.tenyo.co.jp/sheets/tetromino.html)が配布されているが、何千通り、何万通りの種類がある回答を紙で管理するのは非現実的である。
（ただし、そもそも難易度が高いパズルのためそうポンポン回答が出てくるものではないが...）

そこで、スマホを使用してカメラで完成したパズルをスキャンし、データとして保存できたら便利なはず。
ついでに、スキャンした回答が過去に保存済みでないかもすぐに確認したい。


# 仕様
- 脳ブロック（レベル1～5）のパズル正解をスマホのカメラでスキャンし、データとして保存、参照できるアプリ
  - スマホアプリ (Android & iOS)
    - by Flutter ?
  - 何かしらのクラウドデータストレージアカウントと連携し、データを保存
    - Google Drive
    - iCloud Drive
    - Dropbox
    - etc.
  - 手動入力機能
  - 画像入力機能
    - カメラだけでなく画像からのスキャンにも対応
  - 紙の記録用紙からのスキャン機能
    - 既存の紙媒体の記録用紙から一括インポートできるようにしたい
  - 既存の回答データに同じものがあったら、その旨通知
  - 実際の製品とピース構成が異なる場合は警告を表示
    - プライベートでの使用を想定しているので警告にとどめる
    - データでは実際の製品のピース構成であるかのチェック結果を保持したい
  - パズルデータ（独自フォーマット）のファイルインポート・エクスポート機能
- パズルの解析処理プログラム
  - それ専用のライブラリとしてスマホアプリとは区別


## 開発予定
1. パズルシミュレーションにより正解数を求めるプログラムの作成
   - 全レベルにおいて正解の組み合わせ数が公式の値と一致するか確認
2. スマホカメラでパズルの状態をスキャンする機能の実験・開発
3. ライブラリの整備
4. スマホアプリの開発