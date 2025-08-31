github用md

# 009_switch.cpp

## 目的
- `switch` 文で複数の値による分岐を学ぶ
- `break` の役割を理解する

```cpp
int rank = 2;

switch (rank) {
    case 1:
        cout << "金賞" << endl;
        break;
    case 2:
        cout << "銀賞" << endl;
        break;
    case 3:
        cout << "銅賞" << endl;
        break;
    default:
        cout << "圏外" << endl;
        break;
}
```

## 実行結果
銀賞

## 学んだこと
- `switch` は特定の値に応じた分岐ができる
- `case` のあとに評価対象を書く必要がある
- `break` を入れないと次の分岐に進んでしまう