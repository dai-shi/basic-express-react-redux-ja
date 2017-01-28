# HMRの動作確認

HMR (Hot Module Replacement)とは、
コード変更から動的にモジュールを置き換える機能です。
React/ReduxではReactのコンポーネントやReduxのreducerを動的に置き換えます。

## ComponentのHMR動作確認

`npm start` で起動して、 http://localhost:3000/ でアプリを開きます。

別ターミナルやエディタで、 src/client/App.jsx を開き、
ファイルを修正してください。

例えば、

```
      <h1>TODOs</h1>
```

を

```
      <h1>TODOs testing HMR</h1>
```

に変更してみましょう。

開いているブラウザで表示が更新されるのを確認しましょう。
この時ブラウザはリロードしていないことがポイントです。

## reducerのHMR動作確認

同様にアプリを開いた状態で、 src/client/reducer.js を開き、
ファイルを修正してください。

例えば、

```
    return {
      ...state,
      todos: [...state.todos, action.todo],
    };
```

を

```
    return {
      ...state,
      todos: [...state.todos, { text: action.todo.text + '!!!' }],
    };
```

に変更してみましょう。

その後アプリの動作が変化していることを確認しましょう。

## 課題

1. 他にも様々な修正を加えてHMRの動作を確認する
