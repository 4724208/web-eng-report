# 第6回 Webエンジニアリング演習レポート
## 学籍番号
　4724208
## `Todo`型の 定義
```ts
export type Todo = {
  id: number;
  title: string;
  completed: boolean;
  dueDate?: string;
};
```
## 未完了件数を 返す 関数の 引数と 戻り 値の 型
```ts
export async function countIncompleteTodos(): Promise<number> {
```
引数はなし、戻り値は `Promise<number>` です。
## 未完了件数の 実行結果
```
未完了のTODO: 1件
```
