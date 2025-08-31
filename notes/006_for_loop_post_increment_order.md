github用md

# 006_for_loop_post_increment_order.cpp

## 目的
- `for` 文の構文内で `i++` を使ったときの処理順を確認する
- ループ本体と更新部分の実行順を見極める

```cpp
//後置インクリメントとforの実行順の確認用

#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 2; cout << "更新: i=" << i++ << endl) {
        cout << "本体: i=" << i << endl;
    }
    return 0;
}
```

## 実行結果
本体: i=1
更新: i=1
本体: i=2
更新: i=2

## 学んだこと
- `for` 文は更新部（3つ目の式）が最後に実行される
- `i++` のタイミングで値がどう変化するかを細かく見るのに適している