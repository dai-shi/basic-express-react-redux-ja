# APIの作成と利用について

express-react-reduxの本来のスタイルとしては、
APIをexpressで書くことが想定されています。

しかし、教材では取り上げませんでしたので、
参考までにざっと手順をまとめます。

1. expressでJSON APIを作成する
2. redux-thunkとsuperagentをインストールする
3. createStoreでredux-thunkを有効にする
4. コンポーネントでイベントが発生したらthunkをdispatchするようにする
5. そのthunkでは、superagentでJSON APIを叩きその結果からアクションにしてdispatchするようにする
