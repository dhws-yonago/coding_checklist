# CSS

## 文法エラーがないこと

- [ ] チェック

## インデントや改行が適切に入っていること

```css
/** 例: **/
/** NG パターン **/
.inner {
  padding: 0 16px;}
@media (min-width: 769px) {
.inner {
  max-width: 1080px;
  margin: 0 auto;
  padding: 0 32px;
}
}
/** OK パターン **/
.inner {
  padding: 0 16px;
}
@media (min-width: 769px) {
  .inner {
    max-width: 1080px;
    margin: 0 auto;
    padding: 0 32px;
  }
}
```

- [ ] チェック

## コード中に全角スペースを含む全角文字がないこと

- [ ] チェック

## 画像などのファイルパスが正しく設定されていること

- [ ] チェック

## **BEM** など命名ルールを使って `class` , `id` がつけられていること

- [ ] チェック

## 単一のセレクタが複数に分かれて記述されていないこと

```css
/** NG 例: **/
/* メディアクエリ内外で分かれているのは OK */
.inner {
  padding: 0 16px;
}
@media (min-width: 769px) {
  .inner {
    max-width: 1080px;
    margin: 0 auto;
  }
  .inner { /* セレクタの重複 */
    padding: 0 32px;
  }
}
```

- [ ] チェック

## 数字で始まる `class` , `id` がないこと

- [ ] チェック
