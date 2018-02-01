## 配列とforeach

配列とは複数の値を収めることができるものである。仕切りのある入れ物のようなものととらえるとイメージしやすいでしょう。

仕切りで区別されたスペースは、数値または文字列で名前を付けることが可能です。数値で識別される配列を「配列」、文字列で識別される配列を「連想配列」と呼びます。

```php
$staffs = ['田村', '大里', '細川', '池田']

$address = [
    '田村' => '東京都',
    '大里' => '茨城県',
    '細川' => '長野県',
    '池田' => '埼玉県',
];
```
![配列](https://user-images.githubusercontent.com/35711528/35656505-1f7f0134-073b-11e8-80c5-aeb54205f36e.png)
![連想](https://user-images.githubusercontent.com/35711528/35656511-255d4bb0-073b-11e8-9f8e-7bdda9e4af9d.png)


foreachは指定された配列・連想配列の要素を取り出して、先頭から順番に処理をする。

foreach（配列）
```php
foreach(配列 as 値変数) {
// ループ内で実行する処理
}
```

```php
$staffs = ['田村', '大里', '細川', '池田']
foreach($staffs as $staff){
    echo $staff;
}
```

![foreacharray](https://user-images.githubusercontent.com/35711528/35656521-2c216f6c-073b-11e8-8845-a94bd57517c6.png)

foreach（連想配列）
```php
foreach(連想配列 as キー変数 => 値変数) {
// ループ内で実行する処理
}
```
```php
$address = [
    '田村' => '東京都',
    '大里' => '茨城県',
    '細川' => '長野県',
    '池田' => '埼玉県',
];

foreach($address as $key => $value) {
    echo "{$key}さんは{$value}出身です。";
}
```

![forachasarray](https://user-images.githubusercontent.com/35711528/35656990-7b7b4824-073d-11e8-9253-760191a1454d.png)

## 課題
```php
$posts = array(
  0 => array(
    "post_title" => "最初の記事",
    "post_excerpt" => "記事の抜粋",
    "post_date" => "2018/01/31",
    "post_author" => "田村"
  ),
  1 => array(
    "post_title" => "2番目の記事",
    "post_excerpt" => "記事の抜粋2",
    "post_date" => "2018/02/01",
    "post_author" => "大里"
  )
);

```
上記の連想配列について以下のhtmlコードが出力されるようなphpコードをforeachを用いて記述してください。
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
