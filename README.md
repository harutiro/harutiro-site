# 使用環境

## 静的サイトジェネレーター
- hugo
- node
- digitalgarden

## アセッツ
- skill-icons
- icons8
- googlefont


# インストール方法

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

# 書き方
iconは以下のサイトを用いて用意をする

## icons8 
こちらのサイトは、フォントとしてiconを追加する
https://icons8.com/line-awesome

## skill-icons
こちらの方はただのhttpsで画像を持ってきているだけ。
https://github.com/tandpfun/skill-icons?tab=readme-ov-file#icons-list