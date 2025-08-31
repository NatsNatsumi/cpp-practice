github用md

# 025_const_cast.cpp

## 目的
- `const_cast`を使って、`const`修飾を外す方法を学ぶ
- **安全な使い方と危険な使い方の違い**を理解する

```cpp
// 025_const_cast.cpp
#include <iostream>
using namespace std;

void print(char* str) {
    cout << str << endl;
}

int main() {
    const char* msg = "Hello";
    // print(msg); // エラー：const char* を char* に暗黙変換できない

    print(const_cast<char*>(msg)); // const_castで変換

    return 0;
}
```

## 実行結果
```
Hello
```

## 学んだこと
- `const_cast`は**constやvolatile修飾子を外す**ためのキャスト
- **リテラルや読み取り専用領域にある文字列に書き込むと未定義動作になる**
- 読み取りだけならOKだが、**書き換える用途では使わない方が安全**

