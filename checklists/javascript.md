# JavaScript

- [ ] 文法エラーがないこと
- [ ] インデントや改行が適切に入っていること

```javascript
/* 例: */
/* NG パターン */
const button = docment.getElementById('button');

const toggleMenu = () => {
const menu = docment.getElementById('menu');
menu.classList.toggle('active');
};

button.addEventListener('click', event => { event.preventDefault();
  toggleMenu();
});
/* OK パターン */
const button = docment.getElementById('button');

const toggleMenu = () => {
  const menu = docment.getElementById('menu');
  menu.classList.toggle('active');
};

button.addEventListener('click', event => {
  event.preventDefault();
  toggleMenu();
});
```

- [ ] コード中に全角スペースを含む全角文字がないこと  
  ※ `"　"` の中などは OK
- [ ] 数字で始まる関数、変数がないこと
- [ ] 変数や関数の命名ルールにばらつきがないこと
- [ ] 複数ページで参照している `.js` ファイルの場合、ページによって発生するエラーがないこと
- [ ] `var` が使われていないこと
  ※ `let` , `const` を使う
- [ ] 同じ意味のコードが複数の記述で書かれていないこと

```javascript
/* 例: 1 */
/* NG パターン*/
/* ↓ 全部同じ意味 */
$(function(){
  // なにかの処理 1
});

jQuery(document).ready(function() {
  // なにかの処理 2
});

jQuery(function(){
  // なにかの処理 3
});
/* OK パターン */
$(function(){
  // なにかの処理 1
  // なにかの処理 2
  // なにかの処理 3
});

/* 例: 2 */
/* NG パターン*/
/* 同じクリックイベントだが複数の書式で書かれている */
$('#gototop').on('click', function () {
  // なにかの処理
});
$('#nav_open').click(function () {
  // なにかの処理
});
/* OK パターン */
$('#gototop').on('click', function () {
  // なにかの処理
});
$('#nav_open').on('click', function () {
  // なにかの処理
});
```