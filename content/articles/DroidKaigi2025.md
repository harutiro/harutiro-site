---
title: DroidKaigi2025に遊びにいきました
date: 2025-09-19
images: [ "/images/stack/DroidKaigi2025.webp" ]
---

画像などが全くないのですが、いつか貼ります。

# DroidKaigi 2025 参加レポート

DroidKaigi 2025は、2025年9月10日（水）から12日（金）までの3日間、ベルサール渋谷ガーデンにて開催されました。今回も最先端のAndroid技術と、日々の開発に役立つ実践的な知見を深く学ぶことができました。

## 登壇内容の感想と要点

いくつかのセッションに参加し、技術的な深掘りや新たな視点を得ることができました。
その中でも、特に印象に残ったセッションをいくつか紹介させてもらいます。

### 1. AndroidとKotlin Multiplatformで産業グレードのRFIDシステムを構築する (9/11)

このセッションは9月11日の11:20から12:00にJellyfishトラックで、Jasveen Sandral氏によって行われました 。このセッションでは、AndroidとKMPを用いて産業グレードのRFIDシステムを構築する技術が紹介されました 。

*   **通信技術の選択:** 通常のUSBやワイヤレス通信に加え、Webシステムを利用した通信方法が取り上げられていました 。特に興味深かったのは、シリアル通信をAndroidからではなく、**Web技術（Web Serial）** から利用している点です 。
*   **Web技術活用の狙い:** Webからシリアル通信を行うことで、クロスプラットフォームでの対応が可能になったり、アプリのインストールが不要になったりといったメリットが考えられます 。これはKMPから呼び出すための技術として利用されているとの理解が得られました 。
*   **技術ブリッジ:** 具体的な流れは「RFID → Webシリアル → JS → Android App → KMP」というものであり 、WebViewからJSの内容を繋げるブリッジが作られたそうです 。
*   **KMPの可能性:** RFIDパーサーなどのロジックは、シリアル通信さえできてしまえば、あとは共有ロジック（KMP）でできてしまうのは嬉しい話だと感じました 。KMPを雰囲気でしか触ってこなかったため、改めてしっかり触ってみたいという意欲が湧きました 。
*   **Web技術の逆輸入:** このWeb技術をブリッジするアプローチは、5G、AI/ML、AR/VRなど、色々なもののWeb技術をモバイルアプリに「逆輸入」できる可能性を感じさせます 。ただし、WebSerialはiOSには対応していないという制約も確認できました 。


<iframe width="768" height="392" src="https://www.youtube.com/embed/15t2mRY1lQY" title="DroidKaigi 2025 - [EN] Building Industrial-Grade RFID Systems with Android and Ko… | Jasveen Sandral" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### 2. UIだけじゃないComposeの可能性 ━ 宣言的に奏でるメロディ (9/11)

このセッションは9月11日の12:20から13:00にLadybugトラックで、usuiat氏によって行われました 。Jetpack ComposeのRuntimeに焦点を当てた、非常に興味深いセッションでした 。

*   **Composeの構造定義:** コンポーザブル関数はUIの表示を直接作っているわけではなく、構造を定義しているという点を改めて確認しました 。表示は「ツリー構造にする→レイアウトを作る→表示する」というフェーズを経ます 。
*   **コンポーズランタイム:** 私はRuntimeについてあまり理解していませんでしたが [7, 21]、このセッションを通じて、**Runtimeを用いると動作まで宣言的に書くことができる**という可能性を知りました 。
*   **動作の管理:** ノードを使って動作を管理できるため、コードがより分かりやすくなりそうだと感じました 。動作までComposeで管理をするという発想は非常に面白く 、最初の実装は大変そうですが、そこさえ乗り越えればすごく綺麗に実装ができそうだと感じました 。

<iframe width="768" height="392" src="https://www.youtube.com/embed/vVkkHxBWhK0" title="DroidKaigi 2025 - [JA] UIだけじゃないComposeの可能性 ━ 宣言的に奏でるメロディ | usuiat" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### 3. ComposeではないコードをCompose化する (9/12)

このセッションは9月12日の11:20から12:00にLadybugトラックで、Kikoso氏によって行われました 。既存のAndroid ViewをJetpack Composeと統合する際の実践的な課題を扱ったセッションです 。

*   **ライフサイクルの管理:** MapViewには複雑なライフサイクルがあり、色々な通知やリスナーがそのままでは呼び出されない問題があります 。
*   **DisposableEffectの活用:** ライフサイクルを監視するために**`DisposableEffect`**を用いるというテクニックを初めて知りました 。
*   **難しさと不安:** ViewとComposeの接続部分のライフサイクル操作は、毎回変なやり方をしていないのか不安になる部分であり 、おかしいやり方をすると簡単に落ちるし、ブラックボックスになりがちです 。
*   **本質的な課題:** 「メモリーの部分やクラッシュの問題は解決をできたとしても、そもそもそこは最初の始まり」という指摘は痛いところを突かれました 。究極的には、ライフサイクルやバンドルを意識しなくてもできるようにならないといけない 。
*   **学習のヒント:** この細かいAndroid Viewとの接続部分を勉強したかったら、Google Mapをリバースエンジニアリングするのが一番よさそうだというアドバイスがありました 。ViewとComposeは違うものと改めて思わないといけない 。

<iframe width="768" height="392" src="https://www.youtube.com/embed/qFRP2QSf3xQ" title="DroidKaigi 2025 - [EN] Composifying Your Not-Compose Code | Kikoso" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### 4. 「どこから読む？」コードとカルチャーに最速で馴染むための実践ガイド〜新メンバーを活躍に導くオンボーディング戦略〜 (9/12)

このセッションは9月12日の12:20から13:00にKoalaトラックで、richako (risako070310)氏によって行われました 。新メンバーがプロジェクトに馴染むための戦略についての実用的なセッションでした 。

*   **新メンバーの課題:** プロジェクトの概要がわからない、ドメイン知識が足らない、ファイルが多いといった課題が挙げられました 。
*   **コードの読み解き方:** データ、UI、機能に分解して読むこと、特に**UIから読んでいく**のは非常に納得感がありました 。アプリのコアのデータクラスを読むことで何が動いているのかがわかり 、`FindUsages`で使われ方を追跡したり、`Layout Inspector`や`Find in Files`を使うといった具体的な手法が紹介されました 。
*   **ドキュメントの重要性:** 遭難を避けるために地図（`Readme.md`やアーキテクチャー図）を作成する重要性が強調されました 。アーキテクチャ図は本当に大事だと自分も思うが、作られていないプロジェクトが多い気がするため、時間がある最初のうちに作っておきたいです 。
*   **文化・思想の共有:** 日々のレビューで思想を伝えること、コードレビューは指摘ではなく対話として捉えることの重要性が示されました 。設計思想の相談やペアプログラミングを用いて、動機的に共有することも有効です 。
*   **オンボーディングのメンテナー:** **オンボーディング資料やドキュメントの古さを修正できるのは新規メンバーだけ**という考え方は非常に新鮮でした 。新メンバー自身がメンテナーになる文化を作っていくことの重要性を感じました 。


<iframe width="768" height="392" src="https://www.youtube.com/embed/d1Y2VSIs-4U" title="DroidKaigi 2025 - [JA] 「どこから読む？」コードとカルチャーに最速で馴染むための実践ガイド〜新メンバーを活躍に導くオンボーディ… | richako (risako070310)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### 5. 衛星元年 スマホ圏外からLEO衛星🛰で安否情報を届けるAndroid DTC (Direct to Cell)完全攻略 (9/12)

このセッションは9月12日の14:20から15:00にJellyfishトラックで、muo氏によって行われました 。衛星通信という特殊な環境下でのAndroidアプリ開発の課題を扱っていました 。

*   **通信の仕組みと特性:** スマホ → 衛星 → 地上の通信拠点という3点で通信をするという仕組みを理解しました 。Starlinkなどの衛星通信は、通信ができる時とできない時がかなりの頻度であり、非常に不安定です 。
*   **OSの制御:** 衛星が見えていてもすぐに通信をしてはいけないという制御がAndroid OS側で必要になることがわかりました 。なぜなら、衛星基地局はかなり遅く、不安定であり、ユーザーからは「繋がっているのに使えない」という体験になりがちだからです 。そのため、なるべく衛星をつなげないようにする制御が行われます 。
*   **オフラインファーストの徹底:** 衛星モードだと使える機能がかなり減るため 、**安定通信を暗黙的に前提とする設計は使えない**ことが強調されました 。広告が繋がらないと死ぬ、Googleログインができていないと詰むといった事態を避けるためにも、データの送受信を通常のアプリサイクルと切り離し、**オフラインでも使える考え方**が重要だと再認識しました 。
*   **開発の課題:** 圏外でないと検証ができないが、圏外では開発ができないというジレンマが語られました 。Termuxを使って開発やデバッグができる可能性についても触れられていました 。

<iframe width="768" height="392" src="https://www.youtube.com/embed/tzESzyfYG3E" title="DroidKaigi 2025 - [JA] 衛星元年 スマホ圏外からLEO衛星🛰で安否情報を届けるAndroid DTC (Direct to Cell)完全攻略 | muo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

## DroidKaigiのブースでの感想

カンファレンス期間中、スポンサーブースでも興味深い情報に触れることができました [15, 26]。

ホンダさんのブースで、**Android Auto用のエミュレーターを無料で誰でもダウンロードできる**ことを初めて知りました。
また、タクシーGoさんのブースでは 、シェアライドの裏側にあるマッチングの難しさや、乗れる場所を決めたときのやり方について直接話を聞く機会がありました。
他にも、ブースではないのですが、コーヒーの整理券として、サーマルプリンターが用いられており、このシステムの開発者さんとお話ができ、サーマルプリンターを用いた経緯などをお話しさせてもらいました！
本当に、色々な情報を共有できて本当に楽しかったです。

また、ブース以外にも、DroidKaigi を楽しめる色々な工夫がされていました！
ネイル体験ができたり、お菓子や飲み物を用いて雑談をするのに楽しませてもらったり、美味しいご飯などが本当にたくさん出てきてとても良かったです！

---

## 今後の展望

今回、Slackで書いたメモを元にNotebookLMを用いて簡単に記事を書いてみました。
登壇内容と感想と要点以外は、全て手書きの内容になります。
自分の理解度が足らず作者が思っているものとは少し違う解釈をしてしまっているところもあるかもしれませんが、その時は連絡を入れていただけるとありがたいです。

今回も本当に技術力の高いセッションをお聞きして、新たな刺激を受けれたり、Androidエンジニアのコミュニティーの一員として、様々な交流を深めることができました！
こういった経験ができたことに感謝をして、現場での開発に活かせれたらと思っています！

また来年もよろしくお願いします。
