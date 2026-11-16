# 第8回 Webエンジニアリング演習　レポート
## 学籍番号
4724208
## コンポーネント構成

```tsx
import type { Todo } from "../types";

type TodoItemProps = {
    todo: Todo;
};

export function TodoItem({ todo }: TodoItemProps) {
  const isOverdue = todo.dueDate
   ? new Date(`${todo.dueDate}T23:59:59`) < new Date()
   : false;

  return (
    <li>
        <span>{todo.title}</span>
        <span> {todo.completed ? "(完了)" : "(未完了)"}</span>
        {todo.dueDate && (
            <span style={{ color: isOverdue ? "red" : "inherit", marginLeft: "0.5em" }}>
                期限: {todo.dueDate}
            </span>
        )}
    </li>
   );
}
```
## `TodoItem`のProps型

```
type TodoItemProps = {
    todo: Todo;
};
```

## 期限あり・なしの演習画面確認結果

React TODO
Reactを学ぶ (完了)期限: 2026-11-01(赤文字）
Propsを確認する (未完了)期限: 2026-12-31
Stateを更新する (未完了)
