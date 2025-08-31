github用md

# 011_array_basic.cpp

## 目的
- 配列（array）の宣言と初期化の基本を学ぶ
- 複数の同じ型の変数をまとめて扱う方法を理解する

```cpp
int scores[3] = {85, 90, 78};

cout << scores[0] << endl;
cout << scores[1] << endl;
cout << scores[2] << endl;
```

## 実行結果
85
90
78

## 学んだこと
- 配列は同じ型の複数のデータをまとめて扱える
- `scores[0]` のようにインデックスでアクセスする（0始まり）
- 初期値は `{}` でまとめて設定できる