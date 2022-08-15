# R-Funamoto_Gulp_Dart-Sass_EJS
* 当ファイルはDart Sass, EJS対応のgulpfileです。

## 手順
1. ターミナルを起動する
2. cdコマンドで_gulpフォルダに移動する
3. 「npm i」コマンドを実行し、package-lock.jsonとnode_modulesを生成する
4. 「npx gulp」コマンドを実行し、Gulpを起動させる

## 注意点
* 開発フォルダは_assetsです。
* _assetsフォルダ内のファイルは_static/distフォルダに吐き出されます。

## Nodeについて
* node v16.14.0にて動作を確認済。

## Sass
* 当ファイルはDart Sass対応ですが、globでまとめられるようにしておりますので、globalフォルダ以外の各フォルダ内のファイルを_index.scssでまとめる必要はございません。
* 当ファイルは、FLOCSS記法に準じたファイル構成になっております。
* globalフォルダには、変数、関数、mixin等が格納されております。
* 各ファイルでglobalフォルダ内の変数等を使用する場合は、@use "global" as *;の記述が必要です。※相対パスで書く必要はございません。
* objectフォルダ内には、component, project, utilityフォルダがあります。
* pageフォルダには、各ページ固有のCSSを定義したファイルを格納します。
* structureフォルダには、JSライブラリのCSSを格納します。

## EJS
* _assets/ejs/commonフォルダ内には、ヘッダー、フッター等の共通パーツを格納します。
* _assets/ejs/dataフォルダには、各ページのタイトル、ディスクリプション等を管理しているJSONファイルが格納されております。
