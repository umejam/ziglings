# Ziglings Day 9

## 027 defer

* 関数呼び出し時に`defer`を指定すると、指定された関数はブロックを抜けた後に実行される

## 028 defer2

* 複数の`return`文がある場合、`defer`を使えばいずれの場合でも必ず最後に実行する処理を指定出来る

<!-- cSpell: disable-next-line -->
## 029 errdefer

<!-- cSpell: disable-next-line -->
* エラーが発生したときのクリーンアップ処理など、エラーが発生したときだけ最後に実行したい処理を指定するのに`errdefer`がある

## 030 switch

* 式の値による分岐には`switch`文がある
* いずれの値にもマッチしない場合の処理は`else`で指定する

## 031 switch2

* `switch`は式でもある

## 032 unreachable

* 実行されてはならない分岐を示すのに`unreachable`文がある

<!-- cSpell: disable-next-line -->
## 033 iferror

* 以下の構文で`if`文の条件式の値がエラーか否かで分岐させることが出来る

  ```zig
  if (x) |value| {
    // 正常値の処理
  } else |err| {
    // エラー
  }
  ```

* さらに`switch`を組み合わせることも出来る

  ```zig
  if (x) |value| {
    ....
  } else |err| switch (err) {
    ....
  }
  ```
