# Ziglings Day 1

## 001 hello

* 関数のスコープのデフォルトはprivate(ファイルローカル)
* main関数はpublicでないといかん
  ```shell
  $ zig run 001_hello.zig
  lib/std/start.zig:546:45: error: 'main' is private
      switch (@typeInfo(@typeInfo(@TypeOf(root.main)).Fn.return_type.?)) {
                                              ^
  ./001_hello.zig:19:1: note: declared here
  fn main() void {
  ^
  ```
  * public(external)にするには先頭に`pub`を付ける

## 002 std

* ライブラリを使うときは`@import`関数でインポートしなければならない
* `@import`はインポートされたコードを表すconst値を返す
  ```shell
  $ zig run 002_std.zig
  ./002_std.zig:14:1: error: variable of type 'type' must be constant
  var std = @import("std");
  ^
  ```
  * `@import`の戻り値を受け取る変数の名前はインポートしたライブラリ名に合わせるのが慣例
