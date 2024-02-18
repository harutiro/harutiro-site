# 使用環境

## 静的サイトジェネレーター
- hugo
- node
- digitalgarden

## アセッツ
- [skill-icons](https://github.com/tandpfun/skill-icons)
- icons8
- googlefont


# インストール方法

## 初回起動

```bash
# テンプレートのダウンロードを行う
git submodule update --init --recursive
# テーマに必要なパッケージをインストールします
npm install 
# Hugo ビルドで PostCSS を使用するために実行します。
npm i -g postcss-cli
# hugoを起動させる
npm run dev
# or
hugo server
```

## buildを通すとき

tailwindを使用する関係で、このやり方でないと失敗する。

```bash
npm run build
```

# 書き方
iconは以下のサイトを用いて用意をする

## icons8 
こちらのサイトは、フォントとしてiconを追加する
https://icons8.com/line-awesome

## skill-icons
こちらの方はただのhttpsで画像を持ってきているだけ。
https://github.com/tandpfun/skill-icons?tab=readme-ov-file#icons-list