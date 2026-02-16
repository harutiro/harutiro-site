---
title: 人の入り見れる蔵 〜部室の人数をリアルタイム表示〜
date: 2022-06-01
images: ["/images/stack/hitonoirimireru.png"]
description: iBeaconとFirebaseを用いて部室の人数をリアルタイムで表示するサービス。技育キャンプvol.3で努力賞、技育展でも登壇。
icons: ["https://skillicons.dev/icons?i=kotlin" , "https://skillicons.dev/icons?i=androidstudio" , "https://skillicons.dev/icons?i=firebase" , "https://skillicons.dev/icons?i=raspberrypi"]
---

# 人の入り見れる蔵 〜部室の人数をリアルタイム表示〜

2022年 サポーターズ技育キャンプvol.3にて努力賞を受賞し、2022年 技育展「世の中を便利にする」部門でも登壇した作品です。

---

## 概要

iBeaconとFirebaseを活用して、部室にいる人数をリアルタイムで表示するサービスです。

サークルの部室に行ったのに誰もいなかった、という経験を解決するために開発しました。Raspberry Piとビーコンを部室に設置し、入退室を検知してスマートフォンからリアルタイムで人数を確認できます。

---

## 技術スタック

| レイヤー | 技術 |
|---|---|
| ビーコン検知 | iBeacon |
| サーバー | Raspberry Pi |
| データベース | Firebase Realtime Database |
| モバイル | Android (Kotlin) |

---

## 主な機能

- **リアルタイム人数表示**: 部室にいる人数をスマホから確認
- **入退室検知**: iBeaconを用いた自動検知
- **履歴表示**: 過去の在室状況を確認可能

---

## 発表資料

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTxCw3LPuDj4pV8ksbBC-5Ze-sL9pV-1RCaaAU_Rr7ZUFqocH-HzgghQdXoZq1iCFZsvkuScnMdRctJ/pubembed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

[発表資料を直接開く（Google Slides）](https://docs.google.com/presentation/d/1nJJlpBWSvy_7nI_vquOpmU6FeEDkan8svN1KiU5exuY/edit?usp=sharing)
