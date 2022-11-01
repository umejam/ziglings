# Ziglings Day 8

## 021 errors

* `error`型はエラーを表す
  * エラーの種類を表すシンボルの集合

## 022 errors2

* HaskellのMaybe型のような、エラーになる可能性があることを表す型としてerror union型がある
  * `エラーの型!値の型`で表す

## 023 errors3

* `func`がerror unionを返すとき、`func() catch x`と書くと`func`がエラーを返したときは`x`が戻り値となる

## 024 errors4

* 以下の構文で、`catch`を使ってエラーを捕捉出来る

  ```zig
  func() catch |err| {
    if (err == ....) {
        ....
    }
  }
  ```

## 025 errors5

* `f() catch |err| return err`という、エラーを捕捉した場合にはエラーを返して処理を終えるというのは頻出するので、糖衣構文として`try`が用意されている
  * `try f()`は上記と同じ動作になる

## 026 hello2

* `!値の型`を指定すると、なにかしらのエラーを返す可能性があることを表すことが出来る
