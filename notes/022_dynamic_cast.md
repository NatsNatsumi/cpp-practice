github用md

# 022_dynamic_cast.cpp

## 目的
- C++の`dynamic_cast`を使って、安全にポインタを型変換する方法を学ぶ
- ランタイム型情報（RTTI）を活用する場面を理解する

```cpp
// 022_dynamic_cast.cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void speak() {
        cout << "動物が鳴く" << endl;
    }
    virtual ~Animal() {}
};

class Dog : public Animal {
public:
    void speak() override {
        cout << "ワンワン！" << endl;
    }
    void bark() {
        cout << "吠える！" << endl;
    }
};

void tryCast(Animal* a) {
    Dog* d = dynamic_cast<Dog*>(a);
    if (d != nullptr) {
        d->bark();
    } else {
        cout << "Dogじゃないよ" << endl;
    }
}

int main() {
    Animal* a1 = new Dog();
    Animal* a2 = new Animal();

    tryCast(a1); // Dogとしてbarkできる
    tryCast(a2); // Animalなのでcast失敗

    delete a1;
    delete a2;
    return 0;
}
```

## 実行結果
```
吠える！
Dogじゃないよ
```

## 学んだこと
- `dynamic_cast`は、**ポインタ型を安全にダウンキャスト**する手段
- RTTI（実行時型情報）を有効にするには、**仮想関数を含む基底クラスが必要**
- 失敗時は`nullptr`が返るので、**安全にキャスト失敗を判定できる**

