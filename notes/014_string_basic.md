github用md

# 014_string_basic.cpp

## 目的
- `string` クラスの基本的な使い方を学ぶ
- 文字列の代入・結合・出力を体験する

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string firstName = "なつみ";
    string lastName = "よしむら";
    string fullName = lastName + " " + firstName;

    cout << "名前: " << fullName << endl;
    return 0;
}
```

## 実行結果
名前: よしむら なつみ

## 学んだこと
- `#include <string>` を使うことで `string` クラスが使える
- `string 変数名` で文字列を保持できる
- `+` 演算子で文字列同士を結合できる
- `cout` でそのまま文字列を出力できる