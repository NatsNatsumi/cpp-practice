github用md

# 007_variable_assignment.cpp

## 目的
- 変数の代入と更新の基本を理解する

```cpp
//変数の書き換え

#include <iostream>
using namespace std;

int main() {
    int x = 10;
    x = x + 5;
    cout << x << endl;
    return 0;
}
```

## 実行結果
15

## 学んだこと
- 変数に新しい値を代入して更新できる
- `x = x + 5` はよくあるパターン