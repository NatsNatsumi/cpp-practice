github用md

# 017_class_method_split.cpp

## 目的
- `class` 内でメソッド（関数）の定義と実装を分ける方法を学ぶ
- コードの可読性とメンテナンス性を高める設計に慣れる

```cpp
#include <iostream>
#include <string>
using namespace std;

class Player {
private:
    string name;
    int hp;

public:
    Player(string n, int h);
    void showStatus();
};

Player::Player(string n, int h) {
    name = n;
    hp = h;
}

void Player::showStatus() {
    cout << "名前: " << name << endl;
    cout << "HP: " << hp << endl;
}

int main() {
    Player ninja("ナツゴロウ", 150);
    ninja.showStatus();
    return 0;
}
```

## 実行結果
名前: ナツゴロウ
HP: 150

## 学んだこと
- クラス外で `クラス名::関数名` の形で関数定義ができる
- 大規模開発では、ヘッダファイル(.h)と実装ファイル(.cpp)に分けるのが一般的
- 実装の分離により、構造が整理されて保守しやすくなる