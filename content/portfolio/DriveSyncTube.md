---
title: DriveSync Tube
date: 2025-06-01
images: ["/images/portfolio/drivesynctube/top_pc.png"]
description: 車内でYouTubeをみんなで共有できるリアルタイム動画プレイヤー。ホスト（車載モニター）とゲスト（同乗者のスマホ）でプレイリストを共有・操作できるWebアプリです。
icons: ["https://skillicons.dev/icons?i=ts" , "https://skillicons.dev/icons?i=react" , "https://skillicons.dev/icons?i=docker" , "https://skillicons.dev/icons?i=postgres"]
---

# DriveSync Tube

車内でYouTubeをみんなで楽しむためのリアルタイム動画共有プレイヤーです。

**ホスト（車載モニター）** が動画を再生し、**ゲスト（同乗者）** がスマホからリモコンのように動画を追加・操作できます。トンネルや山間部での通信断絶にも対応した堅牢な設計になっています。

サイトURL: [https://dtube.harutiro.net/](https://dtube.harutiro.net/)

GitHub: [https://github.com/harutiro/DriveSyncTube](https://github.com/harutiro/DriveSyncTube)

---

## スクリーンショット

### トップ画面
ルームの作成・参加ができるトップページです。

![トップ画面（PC）](/images/portfolio/drivesynctube/top_pc.png)

![トップ画面（スマホ）](/images/portfolio/drivesynctube/top_sp.png)

### ホスト画面（車載モニター側）
ルームを作成すると表示される再生画面です。QRコードで同乗者を招待できます。

![ホスト画面](/images/portfolio/drivesynctube/host_pc.png)

### ゲスト画面（同乗者のスマホ）
動画の検索・追加・再生操作ができるリモコン画面です。

![ゲスト画面](/images/portfolio/drivesynctube/guest_sp.png)

---

## 使い方

1. **ルームを作成**（ホスト） - トップページで「新しいルームを作成」をタップ
2. **QRコードで招待** - ホスト画面に表示されるQRコードを同乗者が読み取る
3. **動画を検索・追加**（ゲスト） - 検索バーからYouTube動画を検索して追加。URLの直接貼り付けにも対応
4. **みんなで楽しむ** - 再生/一時停止、スキップ、動画の選択・削除がリアルタイムで同期

---

## 技術スタック

| レイヤー | 技術 |
|---|---|
| インフラ | Docker Compose |
| データベース | PostgreSQL 15 |
| バックエンド | Hono, Prisma ORM, WebSocket |
| フロントエンド | Vite, React 19, TypeScript, Tailwind CSS |
| 動画再生 | YouTube IFrame Player API |

---

## 技術的なポイント

### WebSocketによるリアルタイム同期
ホストとゲスト間の状態同期はWebSocketで行い、再生/一時停止・動画追加・再生位置などがリアルタイムで同期されます。

### ネットワーク耐障害性
車内での不安定なネットワーク環境を想定し、以下の対策を実装しています。

- **自動再接続** - 切断時に指数バックオフ（1秒〜最大30秒）で自動再接続
- **ハートビート** - 30秒間隔のPING/PONGでゾンビコネクションを検知
- **サーバー権威モデル** - 再接続時にサーバーから完全同期
- **楽観的UI** - ゲスト操作は即座にUIに反映し、失敗時にロールバック
- **URLベースのルーム復帰** - リロードしても同じルームに復帰
