## 繰り返し処理 for文について
以下が基本的な繰り返し処理 for文の書き方です。
```php
for (初期化式; ループ継続条件式; 増減式) {
    //ループ内で実行する処理
}
```

具体例を見ていきましょう。
```php
<select name="age" id="age">
<?php
    for($i = 10; $i <= 70; $i++) {
        echo "<option value='{$i}'>{$i}歳</option>";
    }
?>
</select>
```

上記のコードは以下のように表示されます。

![for文](https://user-images.githubusercontent.com/20413609/35371050-1ceea660-01d5-11e8-8a99-cf897be0e7ea.png)

## 繰り返し処理 while文について
WordPressにてよく使用される繰り返し処理while文の書き方です。
```php
while(条件式) {
    // 条件がtrueの間繰り返す
}
```

具体例を見ていきましょう。
```php
<select name="age" id="age">
<?php
    $i = 10;
    while($i <= 70) {
        echo "<option value='{$i}'>{$i}歳</option>";
        $i++;
    }
    
?>
</select>
```
上記のコードはfor文で出した例と同じ表示がされます。

WordPressでは以下のような書き方がよく使われています。
```php
<?php while(条件): ?>
… ここが繰り返したい処理 ...
<?php endwhile; ?>
```

## 課題
for文またはwhile文を用いて今月の日にちのセレクトボックスを表示してください。

表示される結果は以下のようにしてください。

![date](https://user-images.githubusercontent.com/20413609/35371071-3ab74c7e-01d5-11e8-849e-aa952bb5c735.png)

**ヒント
date関数を使ってみよう。調べてみよう。
