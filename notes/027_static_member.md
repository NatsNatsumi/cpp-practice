github用md

# 027_static_member.cpp

## 目的
- `static`メンバ変数とメンバ関数の意味と使い方を理解する
- **クラスのインスタンスとは無関係に存在するメンバ**を使う場面を学ぶ

```cpp
// 027_static_member.cpp
#include <iostream>
using namespace std;

class Counter {
    static int count; // staticメンバ変数
public:
    Counter() {
        count++;
    }
    static void showCount() { // staticメンバ関数
        cout << "Count: " << count << endl;
    }
};

int Counter::count = 0; // static変数はクラス外で定義が必要

int main() {
    Counter c1;
    Counter c2;
    Counter::showCount(); // インスタンスを介さずに呼び出せる
    return 0;
}
```

## 実行結果
```
Count: 2
```

## 学んだこと
- `static`を付けたメンバは、**クラスに属するがインスタンスには属さない**
- すべてのインスタンスで共有される（変数）／インスタンスを作らずに呼び出せる（関数）
- 静的変数は**クラス外で初期化が必要**

