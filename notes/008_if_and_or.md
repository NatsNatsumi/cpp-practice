github用md

# 008_if_and_or.cpp

## 目的
- `if`文で複数条件を使う方法を学ぶ
- `&&`, `||`, `!` の使い方を理解する

```cpp
int age = 20;
bool hasLicense = true;

if (age >= 18 && hasLicense) {
    cout << "運転できます" << endl;
} else {
    cout << "運転できません" << endl;
}
```

## 実行結果
運転できます

## 学んだこと
- `&&` は「かつ（AND）」を意味する
- `||` は「または（OR）」を意味する
- `!` は「否定（NOT）」を意味する
- `bool` 型の真偽値は true / false で扱える