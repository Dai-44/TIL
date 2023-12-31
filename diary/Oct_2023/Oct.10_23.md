### ログ
9:37  
- まずはチェリー本から始める。2章の半分くらいまでやったら「教養としての〜」を読んで、READMEアイデア再検討する。アイデアはぶつぶつ独り言いいながら考え深めていきたい。

### ゆる学び
- チェリー本  
  - rubyでは、`=begin`と`=end`を用いることで、その間の複数の行をまとめてコメントアウトすることができる。ただ、主に特定の用途に用いられる記法であるため、基本的には各行の先頭に`#`を記述することが多い。  
  - メソッド呼び出し時に引数を渡す場合、実行するメソッド名と引数の括弧の間にスペースを入れると構文エラーが発生する恐れがある。スペースは空けずに続けて記述する。  
  - 変数の代入は、1行で複数行うこともできる。  
    ```
      a, b = 1, 2
      c, d = 10 # dはnil
      e, f = 100, 200, 300 # 300は切り捨てられる。
    ```  
  - 特別な意味を持つ文字の機能を打ち消し、ただの文字として扱えるようにすることをエスケープ処理という。エスケープしたい文字の前にバックスラッシュを置くことで実現できる。文字列を囲むダブルクォート内で、文字としてダブルクォートを表示させたい場合など。  
  - `==`や`>`などの比較演算子を用いて文字列同士を比較する際、大小比較においては文字列のバイト値を基準に比較がなされる。文字列のバイト値は`bytes`メソッドで確認でき、各文字のバイト値を各要素に持つ配列形式で戻り値が返される。  
  - if文では実行結果が戻り値として返るが、どの条件にも合致しない場合はnilが返る。  
  - メソッド名はアンダースコアで始めることもできる（あまり主流ではないが）。数字で始めることはできず、エラーが発生する。また、キャメルケースはエラーにはならないが一般的ではない。 
- 教養としてのコンピューターサイエンス講義  
  - 1ビットは0または1のどちらかの値を取る数字。オンオフや真偽など、二者択一の選択肢の片方を表現するなら1ビットあれば十分。それ以上の情報を表現する場合には、複数のビットを使用して、0と1による可能な組み合わせに意味を割り当てる。  
