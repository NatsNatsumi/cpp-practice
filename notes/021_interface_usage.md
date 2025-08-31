github用md

# 021_interface_usage.cpp

## 目的
- 純粋仮想関数だけを持つクラス（インターフェース）の定義と利用方法を学ぶ
- クラス間で共通の機能を提供する設計の基礎を理解する

```cpp
// 021_interface_usage.cpp
#include <iostream>
using namespace std;

// インターフェース（純粋仮想関数のみを持つ）
class IPlayable {
public:
    virtual void play() = 0;
    virtual ~IPlayable() {}
};

// 実装クラス1
class Music : public IPlayable {
public:
    void play() override {
        cout << "音楽を再生します" << endl;
    }
};

// 実装クラス2
class Video : public IPlayable {
public:
    void play() override {
        cout << "ビデオを再生します" << endl;
    }
};

int main() {
    IPlayable* media1 = new Music();
    IPlayable* media2 = new Video();

    media1->play();
    media2->play();

    delete media1;
    delete media2;
    return 0;
}
```

## 実行結果
```
音楽を再生します
ビデオを再生します
```

## 学んだこと
- **インターフェース（純粋仮想関数だけのクラス）**は、共通の機能を定義するのに使える
- **`override`**で明示的に継承元の仮想関数を上書きできる
- **インターフェースを通して多態的にオブジェクトを操作**できる（ポリモーフィズム）
- 仮想デストラクタを定義しておくと、delete時に正しく派生クラスのデストラクタが呼ばれる

