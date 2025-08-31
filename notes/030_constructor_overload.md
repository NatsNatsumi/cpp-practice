# 030_constructor_overload.cpp

## 目的
- コンストラクタのオーバーロード（引数違いで複数定義）を学ぶ
- 初期化の柔軟性を確保する

```cpp
#include <iostream>
using namespace std;

class Box {
private:
    int width, height, depth;

public:
    // デフォルトコンストラクタ
    Box() {
        width = height = depth = 0;
    }

    // 1つの値ですべて初期化
    Box(int size) {
        width = height = depth = size;
    }

    // 3つの値で初期化
    Box(int w, int h, int d) {
        width = w;
        height = h;
        depth = d;
    }

    void showVolume() {
        cout << "体積: " << width * height * depth << endl;
    }
};

int main() {
    Box box1;              // 体積 0
    Box box2(3);           // 体積 27
    Box box3(2, 4, 6);     // 体積 48

    box1.showVolume();
    box2.showVolume();
    box3.showVolume();

    return 0;
}
```

## 実行結果
```
体積: 0
体積: 27
体積: 48
```

## 学んだこと
- コンストラクタは引数の数や型を変えて複数定義できる（オーバーロード）
- オーバーロードにより、様々な初期化方法を提供できる
- `Box box2(3);` や `Box box3(2, 4, 6);` のように、状況に応じて柔軟に使える
