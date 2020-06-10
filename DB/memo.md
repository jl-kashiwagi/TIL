# データベースについて学んだことをメモ

- RDBの特徴
  - ロジックの分離
    - Excelはデータとロジックが同じシートに載っているが、RDBはデータ(DB)とロジック(SQL)が分離しているため、一つのデータに対して様々な集計や検索が行える
  - データを柔軟に組み合わせられる
    - Excelは一つのシートに複数のデータを保存できるが、DBではテーブルごとに入れるデータを分け、柔軟に組み合わせることができる。結合されたデータを分離するよりも、分離されたデータを結合するほうがずっと簡単
  - データの整合性を保つ
    - Excelでは他のシートで使用中のデータを削除できるが、RDBでは制限をかけられる
  - データの修正漏れを防ぐ
    - Excelではある社員が結婚して名前が変わった時、その社員が登場する箇所をいちいち変更しなければならない。RDBでは社員テーブルを修正して再結合すればよい
  - RDBでは数十億の大量のレコードを扱える
  - 同時に変更された場合、RDBではトランザクションや変更の競合を検出できる。
    - 複数人が同時にデータを変更する場合、DBを使うべき

- RDBが苦手なこと
  - グラフ作成
  - フォーム入力
  - 帳票機能