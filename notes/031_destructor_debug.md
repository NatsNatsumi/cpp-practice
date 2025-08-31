
github用md

# 031_destructor_debug.cpp

## 目的
- デストラクタの呼び出しタイミングを確認する
- スコープを抜けたときに自動的に呼ばれるかを実験する

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
    cout << "main開始" << endl;
    {
        Sample obj;
        cout << "スコープ内処理中" << endl;
    }
    cout << "main終了" << endl;
    return 0;
}
```

## 実行結果
```
main開始
コンストラクタが呼ばれました
スコープ内処理中
デストラクタが呼ばれました
main終了
```

## 学んだこと
- ブロック（スコープ）を抜けると、ローカル変数のデストラクタが自動で呼ばれる
- 明示的に delete しなくても、自動で破棄される（スタック上のオブジェクト）
