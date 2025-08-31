# C++ Practice Log

これは Unreal Engine や業務で役立つ C++ の基本文法を身につけるための練習ログです。  
主に Paiza.io や Wandbox 上で実行できる簡単なコードを、サンプルと動作確認付きで管理しています。

## 内容まとめ

| 番号 | 内容 | 範囲 |
|------|------|------|
| 001〜007 | 基本文法・演算・条件・ループ | Hello World, if, forなど |
| 008〜015 | 関数・スコープ・参照 | 関数定義、参照渡し、returnなど |
| 016〜020 | クラスの基礎・コンストラクタ | class、メンバ関数、オーバーロードなど |
| 021〜033 | 継承・ポリモーフィズム・ポインタ | 継承、仮想関数、ポインタ、デストラクタなど |


##  内容一覧（001〜033）

| ファイル | 内容 | 補足 |
|---------|------|------|
| 001_hello_world.md | 基本の出力 | `cout`の使い方 |
| 002_add.md | 足し算の基本 | `int` 型変数の演算 |
| 003_if_branch.md | 条件分岐 | `if-else` 文 |
| 004_for.md | 繰り返し処理 | `for` 文の構造 |
| 005_increment_diff.md | インクリメント演算子 | 前置と後置の違い |
| 006_for_loop_post_increment_order.md | for文の実行順序 | 後置インクリメントの挙動 |
| 007_variable_assignment.md | 変数の再代入 | 代入文の意味 |
| 008_if_and_or.md | 複合条件分岐 | `&&`, `||`の使い方 |
| 009_switch.md | switch文 | `case` による分岐処理 |
| 010_function_basic.md | 関数定義の基本 | 引数・戻り値・呼び出し |
| 011_array_basic.md | 配列の基礎 | 配列の宣言と初期化 |
| 012_array_loop.md | 配列のループ処理 | `for` 文での走査 |
| 013_pointer_basic.md | ポインタの基礎 | アドレス参照と間接参照 |
| 014_string_basic.md | 文字列の扱い | `char` 配列と `string` |
| 015_struct_basic.md | 構造体の定義 | `struct` によるデータ構造 |
| 016_class_basic.md | クラス定義の基本 | `class` とオブジェクト指向 |
| 017_class_method_split.md | メソッドの分離 | ヘッダとソースの分割 |
| 018_inheritance_basic.md | 継承の基本 | 親クラスと子クラス |
| 019_polymorphism_virtual.md | 仮想関数と多態性 | `virtual` 関数 |
| 020_abstract_class.md | 抽象クラス | 純粋仮想関数の導入 |
| 021_interface_usage.md | インターフェースの使い方 | クラス設計への応用 |
| 022_dynamic_cast.md | dynamic_cast | 安全なダウンキャスト |
| 023_static_cast.md | static_cast | 静的キャストの用法 |
| 024_reinterpret_cast.md | reinterpret_cast | メモリアクセス型変換 |
| 025_const_cast.md | const_cast | `const` 属性の除去 |
| 026_this_pointer.md | `this` ポインタ | 自身の参照 |
| 027_static_member.md | 静的メンバ | クラスに属する変数/関数 |
| 028_const_member_function.md | constメンバ関数 | 状態を変更しない関数 |
| 029_constructor_destructor.md | コンストラクタとデストラクタ | 生成と破棄の処理 |
| 030_constructor_overload.md | コンストラクタのオーバーロード | 引数違いの初期化 |
| 031_destructor_debug.md | デストラクタでのログ出力 | 破棄時の動作確認 |
| 032_copy_constructor.md | コピーコンストラクタ | 代入とコピーの違い |
| 033_pointer_basics.md | ポインタの基礎復習 | 応用前の振り返り |

# 今後の方針（案）

| 方針 | 内容例 |
|------|--------|
| 実践① | 既習内容で「小さな課題」を作る（電卓、成績管理、構造体で家計簿など） |
| 実践② | STLや標準ライブラリの導入（vector/map/string処理） |
| 実践③ | C++でゲーム要素ぽいミニ演習（ターン制バトル、ダイスゲームなど） |
