github用md

# 016_class_basic.cpp

## 目的
- `class` の基本構文を学ぶ
- `struct` との違いや、アクセス修飾子（`private` / `public`）の役割を理解する

```cpp
#include <iostream>
#include <string>
using namespace std;

class Player {
private:
    string name;
    int hp;

public:
    Player(string n, int h) {
        name = n;
        hp = h;
    }

    void showStatus() {
        cout << "名前: " << name << endl;
        cout << "HP: " << hp << endl;
    }
};

int main() {
    Player hero("ナツミ", 120);
    hero.showStatus();

    return 0;
}
```

## 実行結果
名前: ナツミ
HP: 120

## 学んだこと
- `class` は `struct` と似ているが、メンバのデフォルトが `private`
- `コンストラクタ` で初期値を設定できる（関数名はクラス名と同じ）
- `public` な関数を通して、メンバにアクセスできる
- オブジェクト指向の第一歩として超重要な概念