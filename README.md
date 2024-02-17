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