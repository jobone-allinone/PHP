## 自作関数 

課題2でdate関数という組み込み関数を使いました。PHPには数え切れないほどの組み込み関数があります。

関数は頻繁に使う処理をまとめたもので、自作することもできます。ここで関数を自作してみましょう。

以下が関数を呼び出すための基本的なコードです。
```php
戻り値 = 関数名(引数,・・・)
```

```php
$hoge = getHoge('hoge', 'hogehoge'); //引数が複数ある場合
$fuga = getFuga(); //引数がない場合

hogeFuga(); //戻り値がない場合

function getHoge($hoge, $hogehoge) {
  retrun $hoge + $hogehoge;
}
function getFuga() {
  retrun 'fuga';
}
function hogeFuga() {
  echo 'hogeFuga';
}
```

## 課題
```php
$postsFirst = [
    "post_title" => "最初の記事",
    "post_excerpt" => "記事の抜粋",
    "post_date" => "2018/01/31",
    "post_author" => "田村"
];
$postsSecond = [
    "post_title" => "2番目の記事",
    "post_excerpt" => "記事の抜粋2",
    "post_date" => "2018/02/01",
    "post_author" => "大里"
];

```
上記の連想配列について以下のhtmlコードが出力されるようなphpコードを関数を用いて記述してください。
```html
  <div class='post'>
    <h1>最初の記事</h1>
    <p>記事の抜粋</p>
    <div class='post-meta'>Published on 2018/01/31 by 田村 </div>
  </div>
  <div class='post'>
    <h1>2番目の記事</h1>
    <p>記事の抜粋2</p>
    <div class='post-meta'>Published on 2018/02/01 by 大里 </div>
  </div>
```
