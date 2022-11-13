# Ziglings Day 11

## 37 structs

* C同様、複数の変数をひとつに纏めた構造体を作ることが出来る
* 構造体定義は以下のように`const`変数定義となる

  ```zig
  const 構造体名{ 変数1: 型名, 変数2: 型名, ...};
  ```

* 構造体の初期化構文は以下

  ```zig
  const MyStruct{ x: u8, y: i8 };
  var myStruct = MyStruct{ .x = 10, .y = -3 };
  ```

## 38 structs2
