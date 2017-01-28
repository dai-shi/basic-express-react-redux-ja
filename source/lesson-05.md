# コンポーネントの追加

コンポーネントの追加の手順を覚えましょう。

例えば、 Hello コンポーネントを追加します。

src/client/Hello.jsx を作成し、その中身を

```
import React from 'react';

const Hello = () => <h2>Hello</h2>;

export default Hello;
```

とします。

続いて、 App.jsx に

```
import Hello from './Hello';
```

と、

```
<Hello />
```

を加えましょう。加え方は適切に。

結果を確認しましょう。

## 課題

1. 他にもコンポーネントを追加する
