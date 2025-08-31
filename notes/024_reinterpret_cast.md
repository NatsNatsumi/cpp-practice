github用md

# 024_reinterpret_cast.cpp

## 目的
- `reinterpret_cast`の使い方を知る
- 他のキャストと違い、**メモリ解釈を変更する危険な変換**であることを理解する

```cpp
// 024_reinterpret_cast.cpp
#include <iostream>
using namespace std;

int main() {
    int a = 65;
    char* p = reinterpret_cast<char*>(&a); // intポインタをcharポインタに再解釈

    cout << "int aの最初のバイト: " << *p << endl; // ASCII 'A'として表示されるかも

    return 0;
}
```

## 実行結果
```
int aの最初のバイト: A
```
※結果は環境によって異なる場合あり。

## 学んだこと
- `reinterpret_cast`は**ポインタ型などを強引に別の型に変える**キャスト
- **型安全ではなく、未定義動作の可能性あり**
- **どうしても必要な場面だけで使うべき**危険なキャスト

