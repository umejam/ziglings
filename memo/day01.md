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
