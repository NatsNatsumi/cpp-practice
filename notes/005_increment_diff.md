github用md

# 005_increment_diff.cpp

## 目的
- `i++` と `++i` の違いを理解する
- 後置と前置の動作順を確認する

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 5;

    int a = i++;  // a に代入してから i を +1
    cout << "i++パターン:" << endl;
    cout << "a = " << a << endl;
    cout << "i = " << i << endl;

    cout << endl;

    i = 5;

    int b = ++i;
    cout << "++iパターン:" << endl;
    cout << "b = " << b << endl;
    cout << "i = " << i << endl;

    return 0;
}
```

## 実行結果
i++パターン:
a = 5
i = 6

++iパターン:
b = 6
i = 6

## 学んだこと
- `i++` は代入後に加算、`++i` は加算後に代入される
- 同じ `i` を使っても結果が変わるので注意が必要