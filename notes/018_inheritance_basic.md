github用md

# 018_inheritance_basic.cpp

## 目的
- C++におけるクラスの継承（inheritance）の基本を学ぶ
- 親クラスと子クラスの関係性を理解する
- オーバーライド（関数の上書き）の仕組みを確認する

```cpp
#include <iostream>
#include <string>
using namespace std;

class Character {
protected:
    string name;
public:
    Character(string n) : name(n) {}
    void greet() {
        cout << "やあ、" << name << "だよ。" << endl;
    }
};

class Ninja : public Character {
public:
    Ninja(string n) : Character(n) {}
    void attack() {
        cout << name << "の手裏剣アタック！" << endl;
    }
};

int main() {
    Ninja natsugoro("ナツゴロウ");
    natsugoro.greet();   // 親クラスのメソッド
    natsugoro.attack();  // 子クラスのメソッド
    return 0;
}
```

## 実行結果
やあ、ナツゴロウだよ。
ナツゴロウの手裏剣アタック！

## 学んだこと
- `class Ninja : public Character` で `Character` を継承できる
- 親クラスのメンバ関数を子クラスから呼び出せる
- `protected` にしておくと継承先でもアクセス可能になる
- 子クラスに独自のメソッドを追加できる