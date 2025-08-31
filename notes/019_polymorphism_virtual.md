github用md

# 019_polymorphism_virtual.cpp

## 目的
- C++におけるポリモーフィズム（多態性）を理解する
- `virtual`関数とオーバーライドの動作を確認する
- 親クラスのポインタから子クラスのメソッドを呼び出す方法を学ぶ

```cpp
#include <iostream>
using namespace std;

class Enemy {
public:
    virtual void attack() {
        cout << "敵が攻撃してきた！" << endl;
    }
};

class Ninja : public Enemy {
public:
    void attack() override {
        cout << "忍者が手裏剣で攻撃！" << endl;
    }
};

class Samurai : public Enemy {
public:
    void attack() override {
        cout << "侍が刀で攻撃！" << endl;
    }
};

void battle(Enemy* e) {
    e->attack();
}

int main() {
    Ninja ninja;
    Samurai samurai;

    battle(&ninja);   // 忍者の攻撃
    battle(&samurai); // 侍の攻撃

    return 0;
}
```

## 実行結果
忍者が手裏剣で攻撃！
侍が刀で攻撃！

## 学んだこと
- `virtual` を使うことでポリモーフィズムが機能する
- 親クラスのポインタを使っても、子クラスの `override` メソッドが呼ばれる
- `battle` 関数のように柔軟なインターフェースが作れる
- 仮想関数を使わないと、親クラスのメソッドが呼ばれてしまう