github用md

# 015_struct_basic.cpp

## 目的
- `struct`（構造体）を使って複数の関連する値をまとめて管理する方法を学ぶ
- オブジェクト的なデータの扱い方に慣れる

```cpp
#include <iostream>
#include <string>
using namespace std;

struct Player {
    string name;
    int hp;
    int mp;
};

int main() {
    Player hero = {"ナツミ", 100, 30};

    cout << "名前: " << hero.name << endl;
    cout << "HP: " << hero.hp << endl;
    cout << "MP: " << hero.mp << endl;

    return 0;
}
```

## 実行結果
名前: ナツミ
HP: 100
MP: 30

## 学んだこと
- `struct` を使うことで複数の異なる型の値を1つにまとめられる
- 構造体は変数のように扱え、`.` で各メンバにアクセスできる
- C++における基本的なデータ構造の1つで、ゲームのキャラやアイテムなどによく使う