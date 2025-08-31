github用md

# 026_this_pointer.cpp

## 目的
- `this`ポインタの役割と使い方を理解する
- **クラスの内部で自分自身を指すポインタとしての`this`の意味**を学ぶ

```cpp
// 026_this_pointer.cpp
#include <iostream>
using namespace std;

class MyClass {
    int value;
public:
    MyClass(int value) {
        this->value = value; // 引数のvalueと区別するためにthisを使う
    }
    void show() {
        cout << "value = " << this->value << endl;
    }
};

int main() {
    MyClass obj(42);
    obj.show();
    return 0;
}
```

## 実行結果
```
value = 42
```

## 学んだこと
- `this`は**自分自身のインスタンスを指すポインタ**
- コンストラクタやメンバ関数で、**引数とメンバ変数が被ったときに使う**
- `this`を返してメソッドチェーンに使うこともある

