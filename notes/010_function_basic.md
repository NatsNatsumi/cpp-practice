github用md

# 010_function_basic.cpp

## 目的
- 関数を定義して再利用する方法を学ぶ
- 引数と戻り値の扱いを理解する

```cpp
int add(int a, int b) {
    return a + b;
}

int main() {
    cout << add(3, 5) << endl;
    return 0;
}
```

## 実行結果
8

## 学んだこと
- `int 関数名(引数)` で関数を定義できる
- `return` で戻り値を返すことができる
- `main` 関数から自作関数を呼び出せる