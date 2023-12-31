### ログ
8:39  
- 1時間程度、チェリー本、Paiza、Railsガイドなど勉強系をまず進める。その後、アプリの方向性を考えて技術面談入れる。  


### ゆる学び
- チェリー本  
  - Rubyでは、使われなくなったオブジェクトはガベージコレクションという仕組みによって回収され、その分のメモリは自動的に回収される。プログラマはメモリ管理を意識する必要はない。
    > Rubyのガベージコレクション（GC）は、メモリ管理の一部で、不要になったメモリを自動的に解放する仕組みだナ。  
    >    
    > プログラムを実行していると、オブジェクトが作られてメモリを消費するけど、そのオブジェクトが不要になったらメモリを解放する必要があるダ。でも、これを手動で行うのは非常に難しいダゾ！  
    >     
    > そこでガベージコレクションが登場するダナ。これは、もう使われないオブジェクト（ガベージ）を自動的に見つけ出し、そのメモリを解放する役割を持っているダ。  
    >    
    > この仕組みにより、メモリリーク（不要なメモリが解放されずに溜まってしまうこと）を防ぎ、開発者がメモリ管理に気を使わなくても良い環境を提供してくれるダゾ！   
    >  
    >     
    >  ガベージコレクションは、特に「マーク＆スイープ」というアルゴリズムを使って不要なオブジェクトを見つけ出すダ。
    >  
    > まず「マーク」フェーズでは、プログラムが使っているオブジェクト（ルートオブジェクト）から辿れる全てのオブジェクトをマークするダ。これが「まだ使われているオブジェクト」ってことになるダナ。
    >  
    >  次に「スイープ」フェーズでは、マークされていないオブジェクトをガベージ（ごみ）とみなし、メモリから解放するダゾ。これが「不要になった」という判断になるダカ。
    >  
    >  つまり、オブジェクトがまだ使われているかどうかは、そのオブジェクトがルートオブジェクトから辿れるかどうかで判断されるダナ。
    >
    > オブジェクトが作られるとき、Rubyの内部ではまず必要なメモリのサイズを計算するダ。それからそのサイズ分のメモリ領域を確保するダナ。
    >  
    > メモリの確保は、OSから割り当てを受ける形で行われるダ。メモリは一定の大きさの「ブロック」に分割されていて、オブジェクトが必要とするブロック数をOSに要求するダゾ。
    >  
    > OSは空いているメモリブロックを見つけ、その領域をオブジェクトに割り当てるダ。そして、そのメモリ領域にオブジェクトのデータが格納されるナ。
    >  
    > このように、オブジェクトが作られるときにはメモリの割り当てとデータの格納が行われるダゾ！  
    
  - Rubyでは多くの便利な機能がライブラリとして提供されている。ライブラリには、Rubyが元から用意しておりインストール不要な標準ライブラリ, 組み込みライブラリと、別途インストールが必要な外部ライブラリであるgemがある。インストール不要のライブラリの中でも、組み込みライブラリはデフォルトで利用できるが、標準ライブラリは`require`メソッドで読み込まないと使えない。例えば、`Date`クラスは`date`ライブラリを読み込まないと使えない。  
  - Ruby側で用意されている標準ライブラリであれば`require`メソッドで読み込めるが、自作のライブラリ（別ファイルで定義したクラスなど）を読み込む場合は`require_relative`メソッドを使用して相対パスで対象ファイルを指定する。また、自作ライブラリの読み込みに`require`メソッドを使うこともでき、その場合はパスを`.`から始める。この記法は、カレントディレクトリによって実際に読み込まれるファイルが変わる恐れがあるため推奨されてない（らしい）
  - `puts`メソッドは改行を加えて変数の内容やメソッドの戻り値を出力する。`puts`メソッド自体の戻り値は`nil`。  
  - `print`メソッドは改行を加えずに出力する。  
  - `p`メソッドは改行を加えて出力する。文字列の出力時には””で囲まれて出力される。また、引数で渡されたオブジェクトそのものが戻り値となる。  
  - `pp`メソッドは、大きくて複雑な配列やハッシュを見やすく整形して出力する。例えば、ネストした配列を`p`メソッドで出力すると横並びで見づらいが、`pp`メソッドなら各要素である配列ごとに改行して出力してくれる。戻り値については、`p`メソッドと同様に渡されたオブジェクトとなる。    
  - `puts`と`print`は一般ユーザー向けの出力表示であり、内部で`to_s`メソッドが呼ばれている。一方、`p`と`pp`は開発者向けの出力表示であり、内部で`inspect`メソッドが呼ばれている。`inspect`メソッドは、文字列をダブルクォートで囲んで表示するなど、開発者にとって役立つ情報を返すようになっている。  
  - 配列が渡された場合、`puts`メソッドのみ、各要素の末尾に改行を含む形で要素ごとに行が分けられて表示される。  

