github用md

# 003_if_branch.cpp

## 目的
- C++の条件分岐（`if`, `else`）の基本を理解する
- `>=` 演算子の使い方と `cout` による出力を確認する

```cpp
// 条件分岐（if文）

#include <iostream>
using namespace std;

int main() {
    int age = 17;
    if (age >= 18) {
        cout << "大人です" << endl;
    } else {
        cout << "子どもです" << endl;
    }
    return 0;
}
```

## 実行結果
子どもです

## 学んだこと
- `if` 文で条件を判定し、真の場合のみ特定の処理を実行できる
- `else` を使うことで、条件が偽のときの処理を分けられる
- `>=` は「以上（greater than or equal）」の比較演算子
- `cout` によって結果を表示できる