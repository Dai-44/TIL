### 山浦さんYouTube [JavaScriptの「基礎」が1時間で分かる「超」入門講座【初心者向け】](https://youtu.be/E08jeQBa1D0?si=-Cn_7qdUKvyTW1Ek)
- JSでよく使う`document`や`window`は、JSの機能ではなく、ブラウザAPIが提供しているもの。`document`の場合、そのブラウザの画面に表示されているWebページの内容を指す。JSのコードでそのような`document`などを指定して要素を受け取り、処理を記述できるにすぎない。  
- ブラウザの開発者ツールのコンソール画面で`document`と入力してEnterを押すと、現在画面に表示されている内容のHTMLを取得できる。通常のJSコードで記述するように、`getElementById`などのメソッドを用いれば、特定の箇所の要素を取得できる。  
- ブラウザに表示されたフォーム(`id="input"`)に入力された値を取得するには、`document.getElementById("input").value`のように、取得したDOM要素に`.value`を追加する。  
- `addEventListener`は、特定のイベントが起きた時にJSの処理を追加するためのブラウザAPIの機能。これもJS自体の機能というわけではなく、あくまでブラウザAPIの機能をJSが呼び出して実行している的なイメージ。  
