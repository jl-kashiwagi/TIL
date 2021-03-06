# オブジェクト指向についてメモ

[参考書籍](https://www.amazon.co.jp/%E3%82%AA%E3%83%96%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E6%8C%87%E5%90%91%E3%81%AE%E5%9F%BA%E7%A4%8E-%E3%82%AA%E3%83%96%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E6%8C%87%E5%90%91%E3%81%AE%E5%88%A9%E7%82%B9%E3%82%92%E7%94%9F%E3%81%8B%E3%81%97%E3%81%9F%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%A0%E4%BD%9C%E6%88%90%E3%82%92%E7%9B%AE%E6%8C%87%E3%81%99-%E3%82%B9%E3%82%AD%E3%83%AB%E3%82%BA%E3%83%BB%E3%82%AA%E3%83%B3%E3%83%BB%E3%83%87%E3%83%9E%E3%83%B3%E3%83%89%E7%A0%94%E4%BF%AE%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%A0-%E3%82%A2%E3%82%A4%E3%83%BB%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0-ebook/dp/B00WIMBOQM)

## オブジェクト指向の狙い

- アプリケーションのモデル化を容易にする

- ソフトウェアの構造の詳細を隠蔽する

- 部品化し、それらを組み合わせて開発できるようにする（依存を少なくする）

## オブジェクト指向がなぜ生まれたか

- 以前は構造化がうまくできず、開発効率が悪かった
- オブジェクトという概念がなかった
- データを落とし込んだ開発ができなかった
  - コンピュータの中に「オブジェクト（もの）」の概念を取り込む、オブジェクト指向が生まれた
  - オブジェクト指向によって、データをひとまとめにして扱える

## オブジェクト指向

### オブジェクト / クラス
- オブジェクト
  - システムが関心をもつ対象
  - データとデータに対するメソッドをひとまとめにしたもの
- クラス
  - オブジェクトの型のようなもの
    - データ構造とメソッドをひとまとめに
  - オブジェクトの共通部分を抜き出して定義したもの

### メッセージ / メソッド
- メッセージを送る
  - オブジェクト内の処理を呼び出す
- メソッド
  - メッセージを送ることによって呼び出される操作
- メッセージパッシング
  - オブジェクト間のやりとり
- オブジェクト内の処理は独立
- 自分でできないことは他のオブジェクトに操作を依頼する

### カプセル化 / 情報隠蔽

- カプセル化
  - データ構造と、それに伴う処理をひとまとめに
- 情報隠蔽
  - クラスが持つ情報、データ構造の詳細を外部から見えなくする
  - アクセス制御が便利

カプセル化、情報隠蔽によってシステムに以下のメリットがもたらされる
- 変更容易性
- 保守生産性
- テスタビリティ

### 継承

- 上位クラスの概念を下位クラスに引き継ぐ
- 継承の見つけ方
  - 特化
    - スーパークラス→サブクラス
  - 汎化
    - サブクラス→スーパークラス
  - 抽象化されたクラス

継承はまだそこまで使ってないので、必要性も実感できてなく、あまり理解してない

### 実現
- 仕様を示すインターフェースと、それを実現するクラスの関係
- 実現の見つけ方
  - インターフェースを見つける

インターフェースとは
- インターフェースを実装したクラスに対して、以下のメリットをもたらす
  - 実装の複雑さを隠蔽する
  - 必要なメソッドのみを公開する

実装側に仕様を遵守させる役割を持つ

### 集約
- オブジェクトが他の複数のオブジェクトにより構成されている関係

例: 自動車オブジェクト
- 自動車obj
  - 車輪obj
  - エンジンobj
  - タイヤobj

例の自動車objは複合オブジェクト、車輪objなどがパート（もしくはコンポーネント）・オブジェクトという

コンポーネント・オブジェクトと複合オブジェクトは一体となって存在する

### 依存

- 一方のクラスが他のクラスに影響を及ぼしていること
- 依存の方向は常に一つの方向。双方向はNG
- レイヤ的には下位から上位に依存するように書く

### ポリモーフィズム

- 複数の異なったクラスに同一の名前を持つメソッドを定義し、異なった振る舞いを定義できること
- 動的束縛機能と共に使われることにより効果的に使用できる

### 抽象化
本質的なところを抜き出して、それ以外はポイすること

https://qiita.com/0w0/items/2cfaf3ca0b653960f5e9

- データの抽象化
- メソッドの抽象化

## オブジェクト指向の関連技術

### ソフトウェア・パターン
設計やそのノウハウの再利用を目的として、類型化されたもの

- アーキテクチャー・パターン
- アナリシス・パターン
- デザイン・パターン
- イディオム

### フレームワーク
設計の再利用を目的とした、関連性の強い複数クラスの集合

フレームワークを利用するにあたっての注意点

- 学習曲線
- 適用可能性の検討
- 保守性の検討
- 効率性

### リファクタリング
- Bad smallesに注意

## オブジェクト指向開発のプロセスと表記方法

### UML / RUP

- UML(Unified Modeling Langage)
  - オブジェクト指向分析、設計で用いられる標準モデリング言語
  - 13種類のダイアグラムがある

- RUP (Rational Unified Process)
  - ソフトウェア開発プロセス
