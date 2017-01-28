# アプリの作成

開発の元になるアプリを作成します。

## フォルダの作成

作業用のディレクトリで下記をターミナル(もしくはコマンドプロンプト)で実行します。

```
mkdir sample-app
cd sample-app
```

フォルダ名は好みで変更可能です。

## package.jsonの作成

```
npm init -y
```

手動で作成しても構いません。
`echo '{"scripts":{}}' > package.json` でも可能。

## パッケージをインストールする

```
npm install express express-react-redux --save
```

## テンプレートアプリをインポートする

```
$(npm bin)/express-react-redux import tiny-todos
```

windowsの場合は: `node_modules\.bin\express-react-redux import tiny-todos`

## 開発モードで起動する

```
npm start
```

## アプリを開く

http://localhost:3000/

を開いて動作を確認しましょう

## 課題

1. srcフォルダにあるコードを読む

## 補足

### プロダクションモード

ビルドする

```
npm run build
```

起動する

```
NODE_ENV=production npm start
```
