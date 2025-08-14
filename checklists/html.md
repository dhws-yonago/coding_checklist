# HTML

- [ ] 文法エラーがないこと
- [ ] インデントや改行が適切に入っていること

```html
<!-- 例: -->
<!-- NG パターン -->
<section>
  <div class="container">
  <h2>Title</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore...</p></div>
</section>
<!-- OK パターン -->
<section>
  <div class="container">
    <h2>Title</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore...</p>
  </div>
</section>
```

- [ ] コード中に全角スペースを含む全角文字がないこと  
  ※ 文章中は OK
- [ ] 画像などのファイルパスが正しく設定されていること
- [ ] 外部ファイル (`CSS`, `JavaScript`) が適切な順番で読み込まれていること

```html
<!-- 例: -->
<head>
  <!-- そのほかの要素を省略 -->
  <!--
    1. リセット系 CSS ファイル
    2. ライブラリなどで使う CSS ファイル
    3. 自分で記述した CSS ファイル
  -->
  <link rel="stylesheet" href="https://unpkg.com/sanitize.css">
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
  <link rel="stylesheet" href="./assets/css/common.css">
  <link rel="stylesheet" href="./assets/css/top.css">
</head>
<body>
  <!-- そのほかの要素を省略 -->
  <!--
    1. jQuery本体
    2. ライブラリ本体
    3. 自分で記述した JavaScript ファイル
  -->
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.3/jquery.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>
  <script src="./assets/js/main.js"></script>
</body>
```

- [ ] 1 ページで同一 `id` が複数使われていないこと
- [ ] HTML 内に CSS や JavaScript が書かれていないこと

```html
<!-- NGパターン例: -->
<head>
  <!-- <style> タグにスタイルを記述 -->
  <style>
    .remake {
      color: red;
    }
  </style>
</head>
<body>
  <!-- HTML タグの style 属性でスタイルを記述 -->
  <p style="color:red;">text</p>
  <!-- <script> タグで JavaScript コードを記述 -->
  <script>
    $('#gototop').on('click', function () {
      $('body, html').animate(
        {
          scrollTop: 0
        },
        500
      );
      return false;
    });
  </script>
</body>
```
