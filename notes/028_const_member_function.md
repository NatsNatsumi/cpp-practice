github用md

# 028_const_member_function.cpp

## 目的
- constメンバ関数の構文と意味を理解する
- constを使ったメンバ関数の制約を学ぶ

```cpp
#include <iostream>
using namespace std;

class Sample {
private:
    int value;

public:
    Sample(int v) : value(v) {}

    int getValue() const {
        // value = 100; // エラーになる：const関数内ではメンバを変更できない
        return value;
    }

    void setValue(int v) {
        value = v;
    }
};

int main() {
    Sample s(10);
    cout << "Value: " << s.getValue() << endl;

    s.setValue(20);
    cout << "Updated Value: " << s.getValue() << endl;

    return 0;
}
```

## 実行結果
```
Value: 10
Updated Value: 20
```

## 学んだこと
- constメンバ関数は「この関数ではメンバ変えません」という約束
- const関数内では、メンバ変数を書き換えるとコンパイルエラーになる
- 安全なクラス設計や読み取り専用メソッドに便利
