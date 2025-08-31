github用md

# 023_static_cast.cpp

## 目的
- C++の`static_cast`の基本的な使い方を学ぶ
- 型変換の安全性と用途を確認する

```cpp
// 023_static_cast.cpp
#include <iostream>
using namespace std;

int main() {
    double pi = 3.14159;
    int intPi = static_cast<int>(pi); // 明示的な型変換

    cout << "元の値: " << pi << endl;
    cout << "intに変換: " << intPi << endl;

    char c = 'A';
    int ascii = static_cast<int>(c); // charからint
    cout << "'A'のASCIIコード: " << ascii << endl;

    return 0;
}
```

## 実行結果
```
元の値: 3.14159
intに変換: 3
'A'のASCIIコード: 65
```

## 学んだこと
- `static_cast`は**明示的なコンパイル時の型変換**に使う
- 暗黙変換でも行ける場面を明確に示すことで**可読性と安全性が上がる**
- ポインタや数値型の変換にも使えるが、**不正な変換は自己責任**

