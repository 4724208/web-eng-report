# 第5回　Webエンジニアリング演習レポート
# 4724208

## TODO配列のコード

'''ts
const todos = [
    { id: 1, title: "型を復習する", completed: true },
    { id: 2, title: "配列を学ぶ", completed: false },
    { id: 3, title: "レポートを書く", completed: false },
    { id: 4, title: "レポートを提出する", completed: false},
];
'''

## TODOを更新した条件

'''ts
const completedBefore = todos.filter((todo) => todo.completed).length;
for (const todo of todos) {
 if (todo.completed === false) {
  todo.completed = true;
  console.log(`更新後: ${todo.title} [完了]`);
 }
}
const completedAfter = todos.filter((todo) => todo.completed).length;
console.log(`完了件数: 更新前 ${completedBefore}件 -> 更新後 ${completedAfter}件`);
'''

## 完了件数の更新前後の実行結果

'''
@4724208 ➜ /workspaces/web-eng-typescript (class-05-collections) $ pnpm run start
$ tsx src/index.ts
1: 型を復習する [完了]
2: 配列を学ぶ [未完了]
3: レポートを書く [未完了]
4: レポートを提出する [未完了]
[ { id: 1, title: '型を復習する', completed: true } ]
[ '型を復習する', '配列を学ぶ', 'レポートを書く', 'レポートを提出する' ]
更新後: 配列を学ぶ [完了]
更新後: レポートを書く [完了]
更新後: レポートを提出する [完了]
完了件数: 更新前 1件 -> 更新後 4件
@4724208 ➜ /workspaces/web-eng-typescript (class-05-collections) $ pnpm run check
$ tsc --noEmit
'''
