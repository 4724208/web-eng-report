# 第4回 Webエンジニアリング演習レポート
## 4724208
## `const`と`let`の 宣言・ 再代入に 使用したコード
（コードまたは確認結果）
ts
const courseName = "Web Engineering";
let retryCount = 1;

courseName = "Other Course";
retryCount = 2;

console.log(`${courseName}の再試行回数は${retryCount}回である`);

## VSCodeと`pnpm run check`に表示されたエラー番号・メッセージ
VSCode：
Cannot assign to 'courseName' because it is a constant. ts(2588)
`pnpm run check`：
src/index.ts:23:1 - error TS2588: Cannot assign to 'courseName' because it is a constant.

## 修正後の実行結果と`const`・`let`の違いの説明
実行結果：
Web Engineeringの再試行回数は2回である

constは一度宣言したら型を変えれないので、エラーが出た。
letは後から値を変えられるのでエラーは出なかった。
