### ログ
10:19  
- 昨日話したことによって、自分がアイデア出す時は奥さんとの日常生活のことを自然に考えているという気づきが得られた。日常の中で鬱陶しくないレベルで使いたいと思うアプリを考え、開発していく。そっちの方が楽しめそう。  

### ゆる学び
- チェリー本（p.153~）  
  - `upto`メソッドは、レシーバの数字から引数で渡す数字まで数値を一つずつ増やしながら、同じ処理を繰り返したい場合に利用できる。`downto`メソッドは逆に、数値を一つずつ減らしながら処理を繰り返す。  
      ```
      a = []
      10.upto(15) { |n| a << n }
      
      a #=> [10, 11, 12, 13, 14, 15] 
      ```
  - `while`文も`if`と同じように後置できる。  
      ```
      a = []
      a << 1 while a.size < 5
      
      a #=> [1, 1, 1, 1, 1]
      ``` 
  - `break`は繰り返し処理からの脱出、`return`は繰り返しに限らずメソッドからの脱出。  
- Zenn Railsハンズオン  
  - `Rubocop`の自動修正は便利なので活用すべきだが、意図しない箇所まで変更される恐れもあるため、直前にcommitしておくと良い。  
