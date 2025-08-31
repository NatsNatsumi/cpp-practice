github用md

# 032_copy_constructor.cpp

## 目的
- コピーコンストラクタの基本を理解する
- オブジェクトを引数に渡す際の動作確認

```cpp
#include <iostream>
using namespace std;

class MyClass {
public:
    int value;
    MyClass(int v) : value(v) {
        cout << "通常のコンストラクタ: " << value << endl;
    }

    MyClass(const MyClass& other) {
        value = other.value;
        cout << "コピーコンストラクタ: " << value << endl;
    }
};

void show(MyClass obj) {
    cout << "show関数内: " << obj.value << endl;
}

int main() {
    MyClass a(10);
    show(a);
    return 0;
}
```

## 実行結果
```
通常のコンストラクタ: 10
コピーコンストラクタ: 10
show関数内: 10
コピーコンストラクタ: 10
```

## 学んだこと
- `MyClass(const MyClass& other)` の形式でコピーコンストラクタを定義できる
- オブジェクトを値渡しするとコピーコンストラクタが呼ばれる
- 値渡し・戻り値による一時オブジェクト生成でもコピーされる場合がある
