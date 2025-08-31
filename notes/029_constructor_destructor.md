github用md

# 029_constructor_destructor.cpp

## 目的
- コンストラクタとデストラクタの役割を知る
- オブジェクト生成と破棄のタイミングを確認する

```cpp
#include <iostream>
using namespace std;

class Sample {
public:
    Sample() {
        cout << "コンストラクタが呼ばれました" << endl;
    }
    ~Sample() {
        cout << "デストラクタが呼ばれました" << endl;
    }
};

int main() {
    Sample s;
    cout << "main関数の中です" << endl;
    return 0;
}
```

## 実行結果
```
コンストラクタが呼ばれました
main関数の中です
デストラクタが呼ばれました
```

## 学んだこと
- コンストラクタはオブジェクト生成時に自動で呼ばれる
- デストラクタはオブジェクトが破棄されるときに自動で呼ばれる
- 明示的に呼び出さなくても動作する
