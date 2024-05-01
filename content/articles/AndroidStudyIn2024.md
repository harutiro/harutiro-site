# 環境について
今回のAndroidStudioのバージョンは`Android Studio Jellyfish | 2023.3.1`でやっていきます。

<img width="450" alt="image.png (120.6 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2024/05/02/129607/c852792c-03a0-4245-a48e-408f9f224ea6.png">

最近のバージョンだとGeminiを用いてAIと対話しながら開発ができるらしいです。
使ったことはないのでどれくらい精度がいいかはわかりませんが、GitHubCopilotくんを使うお金がない方などは使ってみてもいいかもしれないです。
<img width="627" alt="スクリーンショット 0006-05-02 0.25.50.png (303.4 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2024/05/02/129607/aa71ee20-7697-43c8-bfd4-78a890a82b22.png">


とりあえず、最新を使いましょう。

[インストールリンク](https://developer.android.com/studio?hl=ja&_gl=1*160el0k*_up*MQ..*_ga*Mzk0Nzg2Nzg0LjE3MTQ1NzY3MzE.*_ga_6HH9YJMN9M*MTcxNDU3NjczMC4xLjAuMTcxNDU3NjczMC4wLjAuMA..)

# 最初の導入 モバイル開発とはどんな感じかをお話しします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSUYHaglKjkocTvVgLCKw5Np0DlzyVuDR6EtEP6XvlCDhbxPmuVkm45SiZ5Z4NitAO4jxTY8XYJyQGj/embed?start=false&loop=true&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

[スライドリンク](https://docs.google.com/presentation/d/1wgY9WbdLNKvvWbbJlmStjmwVL3vXPX_CoIOe4G8A7Gk/edit?usp=sharing)

# おすすめの本
- おすすめの本
  - 初めてのAndroidプログラミング
  <img width="300" alt="71ce43XdxlL.jpg (231.8 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2021/06/10/84962/cfe0ba13-5889-4a67-86f0-d16e41eae674.jpg">

# AndroidDevelopersは便利だよ
ちょっと前までは英語の記事だったり、少しわかりずらいなどがありましたが、今はすごくわかりやすくいい記事がたくさんあります。
ぜひ、ここの公式サイトを色々みてみると面白いかもしれないです。
https://developer.android.com/?hl=ja

# ライフサイクルは大事(よくわからなかったら飛ばしてもOK)
- ただのJavaのプログラムとAndroidのアプリの違いは？
- Androidアプリには、端末サイドでアプリを起動した時、アプリを立ち上げた後にホームに戻った時、アプリをタスキルした時とかタイミングがある。

<img width="513" alt="activity_lifecycle.png (45.7 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2021/07/09/84962/06cd2b16-5e50-4bf5-9102-51d265ba0a53.png">

- ↑アクティビティのライフサイクル。
- アプリは起動すると、作られて、始まって、、、みたいなの。

# 具体的な内容

以下の記事をみなさんに進めてもらいます。
その中でわからないところがあったら、適宜教えにいくスタイルにします。
残り1時間ぐらいになったら、今できている範囲で何か面白いひと工夫をWebなどで調べながら実装してもらって、少し発表会をして終わる感じにします。

- [AndroidでHelloWorld](https://developer.android.com/codelabs/basic-android-kotlin-compose-first-app?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-compose-unit-1-pathway-2%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-compose-first-app&%3Bhl=ja&hl=ja#0)
    - とりあえず、アプリを作ってみて、出力される文字を変えてみるだけ。
    - 動作確認だけです。
- JetpackComposeで画面の表示の基礎
    - わかるところは飛ばして進めます。
    - 一部いらないところはスキップしていきます。
    - [ユニット 1: 初めての Android アプリ](https://developer.android.com/courses/android-basics-compose/unit-1?hl=ja)
    - [ユニット 2: アプリ UI を作成する](https://developer.android.com/courses/android-basics-compose/unit-2?hl=ja)
    - [ユニット 3: リストの表示とマテリアル デザインの使用](https://developer.android.com/courses/android-basics-compose/unit-3?hl=ja)
- Androidを使いこなす
    - [ユニット 5: インターネットに接続する](https://developer.android.com/courses/android-basics-compose/unit-5?hl=ja)
    - [ユニット 6: データの永続化](https://developer.android.com/courses/android-basics-compose/unit-6?hl=ja)
    

