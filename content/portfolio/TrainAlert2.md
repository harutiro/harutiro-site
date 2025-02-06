---
title: TrainAlert2「トレアラ」～電車乗り過ごし防止アプリ～
date: 2022-03-12
images: [ "/images/portfolio/icons/TrainAlert2.png" ]
description: もう寝過ごさない、降りる駅に近づくと自動的にアラートを出すアプリのリメイク版
icons: ["https://skillicons.dev/icons?i=kotlin" , "https://skillicons.dev/icons?i=androidstudio", "las la-map"]
---

#  作品概要

作業期間：約3ヶ月
関係者人数：4人
担当役割：開発サポート、リリース、プロジェクトマネージャー、アイディア出し
使用技術：Android、Kotlin、Jetpack Compose、Room
プロジェクトURL
https://github.com/kajiLabTeam/TrainAlert2

# アプリの特徴
電車内でうとうとして乗り過ごしを防ぐために、降りる駅が近づくと自動的にアラートを発するアプリです。面倒なタイマー設定が不要で、事前に目的地を設定しておくだけで利用できます。Google Maps APIを活用し、直感的に駅を選択して登録できるようにしました。

### 開発のきっかけ
このアプリは、高校時代に作成した「TrainAlert」のリメイク版です。位置情報やHuman Computer Interaction（HCI）に関心を持つ研究室での勉強として開発を開始し、位置情報の利用方法やフィードバックの設計を学ぶ良い機会となりました。また、過去の作品を自分の知識で再構築したいという思いもあり、Android ViewからJetpack Compose、RealmからRoomに変更し、クリーンアーキテクチャを意識したフォルダ構成に刷新しました。

以前のアプリ
過去に作成したバージョンも以下でご覧いただけます。
https://play.google.com/store/apps/details?id=app.makino.harutiro.trainalert

# 自分の役割と技術面で最も苦労した点・工夫した点

### 担当分野・使用技術
私の役割は、開発サポート、リリース準備、プロジェクトマネジメント、アイディア出しなど幅広く担当しました。また、AndroidとKotlinを用い、Jetpack ComposeやRoomといった最新技術を活用しながら、アプリの設計と開発に携わりました。

### 技術面での工夫
チームで進める中で、各メンバーが学びながら参加できるように配慮しました。技術力の差が生まれがちですが、定期的なミーティングやペアプロを実施し、理解度のギャップを埋めつつプロジェクト全体を進めました。メンバーが置いていかれないよう、チーム全体での成長を目指したことが成果につながったと感じています。

### 最も苦労した点
Geofenceを用いた降車駅付近での通知機能の実装です。降車駅の600m手前で通知を発するため、DroidKaigiで私が登壇した内容を使用して、電池消費を抑えつつ精度の高いGeofenceを設定する工夫を凝らしました。また、通知に関しては、通常の通知に加えて音や光、バイブレーションなどを取り入れ、利用者が確実に気づけるような多様なアラート機能を搭載しました。

### 今後の展望
現段階ではバックエンドの不足や使い勝手の改善が必要で、リリースには至っていません。しかし、引き続き更新を行い、リリースを目指しています。また、このアプリを定期的にアップデートし、継続的に改善・発展させていく予定です。


# 発表資料
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTDZSHJ29sa8ME7Kr0JZJr5MuCd-JVeNR33wDKdAVGy7wiA2L61Svi0CIKvtDaK_IyQ6izVTr0KrSO4/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>