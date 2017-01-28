# reducerの追加

reducerの追加の手順を覚えましょう。

例えば、項目を削除する機能を追加します。

reducer.js に下記を追加します。

```
  if (action.type === 'DELETE_TODO') {
    const index = action.index;
    const todos = state.todos;
    return {
      ...state,
      todos: [].concat(todos.slice(0, index), todos.slice(index + 1)),
    };
  }
```

## 課題

1. 項目を削除する機能を App.jsx に実装しましょう

## 補足

reducerを分割して実装する場合には、しばしばcombineReducersを使います。
詳しくは、[公式ドキュメント](http://redux.js.org/docs/api/combineReducers.html)を参照してください。
