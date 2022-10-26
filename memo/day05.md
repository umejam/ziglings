# Ziglings Day 5

## 011 while

* `while`文の条件式を囲う`()`は必須

## 012 while2

* 以下の形で繰り返しのたびにボディの最後に実行する式を指定できる。これを`continue`式と呼ぶ

  ```zig
  while (condition expression) : (continue expression) {
    ....
  }
  ```

## 013 while3

* Cと同じようにボディに`continue`文を書くことが出来る
* `continue`式は、`continue`文の有無に関わらず、ボディの最後に実行される

## 014 while4

* Cと同じようにボディに`break`文を書くことが出来る
* `break`文が実行された場合は、`continue`式は実行されない
