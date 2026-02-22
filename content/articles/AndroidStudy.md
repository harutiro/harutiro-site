---
title: Androidを勉強してみようの記事 in 2026
date: 2026-02-22
images: [ "https://img.esa.io/uploads/production/attachments/13979/2024/05/02/129607/c852792c-03a0-4245-a48e-408f9f224ea6.png" ]
---
# 環境について
今回のAndroidStudioのバージョンは`Android Studio Ladybug | 2024.2.1 Patch 3`でやっていきます。

<img width="1276" alt="image.png (107.5 kB)" src="https://img.esa.io/uploads/production/attachments/19973/2025/02/24/129607/db333278-42db-456a-8ba2-97060d70ab01.png">

最近のバージョンだとGeminiを用いてAIと対話しながら開発ができるらしいです。
そこそこ精度が良く、自動補完などもあるので時間があれば使ってみるのもいいかもしれないです。

<img width="627" alt="スクリーンショット 0006-05-02 0.25.50.png (303.4 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2024/05/02/129607/aa71ee20-7697-43c8-bfd4-78a890a82b22.png">

とりあえず、最新を使いましょう。

# インストール方法

インストール方法としては、JetbrainsToolBoxを用いてAndroidStudioを入れた方が最新のバージョンに上げやすいのでかなりおすすめです。
ですが、初めて使う人は二つもアプリを入れないと行けなくなり、混乱すると思うので、その場合はこのやり方はしなくても大丈夫です。

### JetbrainsToolBoxを用いたインストール方法
[インストールリンク](https://www.jetbrains.com/ja-jp/toolbox-app/)
JetbrainsToolBoxを入れてそこからAndroidStudioを入れてください。

### 通常のインストール方法
<img width="1680" alt="スクリーンショット 0007-02-24 21.39.31.png (439.5 kB)" src="https://img.esa.io/uploads/production/attachments/19973/2025/02/24/129607/60949b5b-9c08-429d-ad8c-3be98b3898dc.png">

[こちら](https://courses.codeforfun.jp/courses/kotlin-intro-for-android/lectures/47723564)から開発環境の設定をお願いします。
code for fun と呼ばれるかなり便利そうなサイトがあったのでこちらで使わせていただきます。
開発環境の設定は以下の画像に載っている範囲(Andoroid Studioのインストール 〜【補足】エミュレータの悪性方法)まで行ってください。

# 最初の導入 モバイル開発とはどんな感じかをお話しします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSUYHaglKjkocTvVgLCKw5Np0DlzyVuDR6EtEP6XvlCDhbxPmuVkm45SiZ5Z4NitAO4jxTY8XYJyQGj/embed?start=false&loop=true&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

[スライドリンク](https://docs.google.com/presentation/d/1JJitW0OkT-MzQQBUkDoDZ_V9e1MXiYmIHmEf9KhnSJ4/edit?usp=sharing)

# [コラム] おすすめの本
### イチからはじめるAndroidプログラミング: Kotlin知識ゼロOK！Jetpack Compose対応！ (コードマスターシリーズ)

初心者向きのAndroidの本です。
AndroidStudioのインストール方法から、Kotlinの基礎、簡単なアプリの作り方まで全て入っています。
JetpackComposeと呼ばれる最近のナウイ技術まで入っているのでおすすめです。

購入URL : https://amzn.asia/d/dIB9Wiu
 <img width="300" alt="スクリーンショット 0007-02-24 21.43.25.png (742.9 kB)" src="https://img.esa.io/uploads/production/attachments/19973/2025/02/24/129607/989d3feb-fa59-4fda-977f-9bb0023a6c0b.png">
###  詳解 Jetpack Compose ── 基礎から学ぶAndroidアプリの宣言的UI 

JetpackComposeの知識をより深く入れたい人向けの記事です。
Androidを書くのに慣れてきたときに読んでみるのがおすすめです。

購入URL : https://amzn.asia/d/dIB9Wiu
<img width="308" alt="スクリーンショット 0007-02-24 21.44.41.png (662.5 kB)" src="https://img.esa.io/uploads/production/attachments/19973/2025/02/24/129607/cbcbf01a-42de-4b74-957c-d4163fe90bf3.png">

# [コラム] AndroidDevelopersは便利だよ
ちょっと前までは英語の記事だったり、少しわかりずらいなどがありましたが、今はすごくわかりやすくいい記事がたくさんあります。
ぜひ、ここの公式サイトを色々みてみると面白いかもしれないです。
https://developer.android.com/?hl=ja

# [コラム] ライフサイクルは大事(よくわからなかったら飛ばしてもOK)
- ただのJavaのプログラムとAndroidのアプリの違いは？
- Androidアプリには、端末サイドでアプリを起動した時、アプリを立ち上げた後にホームに戻った時、アプリをタスキルした時とかタイミングがある。

<img width="513" alt="activity_lifecycle.png (45.7 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2021/07/09/84962/06cd2b16-5e50-4bf5-9102-51d265ba0a53.png">

- ↑アクティビティのライフサイクル。
- アプリは起動すると、作られて、始まって、、、みたいなの。


# [New!]  SysHack向け短期間でアンドロイドを知ろうスライド

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vREDCx_bvyeyWg3-Fb5TJ9EjArbrabLGq3EzEJjIUrzIvB53Z7mmpmgWky5QZSb1UkJwQvACJuSn-vq/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

[スライドURL](https://docs.google.com/presentation/d/1ytJI67q-OHZtRBvfzUtSWiC9UQ_YHL8xPOvgShjbubA/edit?usp=sharing)

# 具体的な内容

以下の記事をみなさんに進めてもらいます。
その中でわからないところがあったら、適宜教えにいくスタイルにします。
残り1時間ぐらいになったら、今できている範囲で何か面白いひと工夫をWebなどで調べながら実装してもらって、少し発表会をして終わる感じにします。

> [!TIP]
>基本的に全ての資料を完全に理解する必要はないです。
>色々動かしてみてあぁ！！なんか動いたを繰り返していけばOKです。
>いっぱい触っていて、こうやったこう動くのかというどこを触ればどこが動くのかを理解することが大切です。
>そして全てを覚えようとしなくてOKです。また調べればいいのです。

今回の勉強会資料で用いる公式リファレンスのやつ
https://developer.android.com/courses/android-basics-compose/course?index=..%2F..android-kotlin-fundamentals&hl=ja#0

- Android初心者はこちらからどうぞ
    - [AndroidでHelloWorld](https://developer.android.com/codelabs/basic-android-kotlin-compose-first-app?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-compose-unit-1-pathway-2%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-compose-first-app&%3Bhl=ja&hl=ja#0)
    - とりあえず、アプリを作ってみて、出力される文字を変えてみるだけ。
    - 動作確認だけです。
- Androidをすでに触ったことある人向け(**初心者の方は飛ばしましょう**)
    - [Jetpack Compose チュートリアル](https://developer.android.com/develop/ui/compose/tutorial?hl=ja)
    - XMLではAndroidを触ったことあるが、JetpackComposeを触ったことない人はこれから始めるといいでしょう。
- JetpackComposeで画面の表示の基礎
    - わかるところは飛ばして進めます。
    - 一部いらないところはスキップしていきます。
    - [ユニット 1: 初めての Android アプリ](https://developer.android.com/courses/android-basics-compose/unit-1?hl=ja)
    - [ユニット 2: アプリ UI を作成する](https://developer.android.com/courses/android-basics-compose/unit-2?hl=ja)
    - [ユニット 3: リストの表示とマテリアル デザインの使用](https://developer.android.com/courses/android-basics-compose/unit-3?hl=ja)
- Androidを使いこなす
    - [ユニット 4: ナビゲーションとアプリ アーキテクチャ](https://developer.android.com/courses/android-basics-compose/unit-4?hl=ja)
        - こちらに関しては綺麗なプログラミングをする方法
    - [ユニット 5: インターネットに接続する](https://developer.android.com/courses/android-basics-compose/unit-5?hl=ja)
        - HTTP通信、バックエンドと通信をしよう
    - [ユニット 6: データの永続化](https://developer.android.com/courses/android-basics-compose/unit-6?hl=ja)
        - データベースを用いる(Room)
        - これでデータを保存できる
    - [ユニット 7: WorkManager](https://developer.android.com/courses/pathways/android-basics-compose-unit-7-pathway-1?hl=ja)
        - バックグラウンド処理をやる方法
    - [ユニット 8: Compose とビュー](https://developer.android.com/courses/android-basics-compose/unit-8?hl=ja)
        - jetpackComposeとViewを繋げる方法


### 「コラム」kotlinの言語自体を学ぶ

正直、プログラミングをするにあたり言語の特性だったりをしっかり理解する必要はそこまでない。
そのため、そんなにしっかりと構文を理解して、ラムダ式を使ったりSuspendを利用する必要はないが、もし、時間があってそこそこにやる気がある状態ならやるべきだとは思う。
ぜひ、余裕がある時に触って見てはいかがでしょうか？

https://kotlinlang.org/education/
<img width="1680" alt="スクリーンショット 0006-07-24 17.38.57.png (463.3 kB)" src="https://img.esa.io/uploads/production/attachments/13979/2024/07/24/129607/a09a8023-9d8b-416f-b4e4-13c08c225f88.png">
