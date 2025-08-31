github用md

# 020_abstract_class.cpp

## 目的
- 抽象クラスの仕組みと使い方を理解する
- 純粋仮想関数（=0）の意味と効果を学ぶ

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void makeSound() = 0; // 純粋仮想関数
};

class Dog : public Animal {
public:
    void makeSound() override {
        cout << "ワンワン！" << endl;
    }
};

class Cat : public Animal {
public:
    void makeSound() override {
        cout << "ニャー！" << endl;
    }
};

int main() {
    Animal* dog = new Dog();
    Animal* cat = new Cat();
    dog->makeSound();
    cat->makeSound();
    delete dog;
    delete cat;
    return 0;
}
```

## 実行結果
```
ワンワン！
ニャー！
```

## 学んだこと
- `virtual 関数 = 0` と書くと純粋仮想関数になる
- 純粋仮想関数があるクラスはインスタンス化できない（抽象クラス）
- 継承先で `override` して具体的な動作を実装する
- 抽象クラスは共通のインターフェースとして便利
