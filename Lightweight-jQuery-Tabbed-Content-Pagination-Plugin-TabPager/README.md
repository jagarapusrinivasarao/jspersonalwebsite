# jQuery TabPager

jQuery TabPagerはタブの切り替えと、タブ内でのページネーションをAjaxを使わずに実装したjQueryプラグインです。

![Screen Shot](https://raw.github.com/tsuyoshiwebcake/jq-plugin-tab-pager/master/screenshot.png)

  - jQuery 1.7+

## License

MIT License

## Options

| オプション名 | 設定値 | 初期値 | 説明 |
|:--|:--|:--|:--|
| items | Number | 5  | 1ページあたりの最大表示数 |
| contents | String | 'contents'  | タブコンテンツのクラス名 |
| time | Number | 800  | ページ切り替え時のフェードイン時間 |
| previous | String | 'Previous»'  |  	前のページに1つ戻るナビゲーションのテキスト |
| next | String | '«Next'  | 次のページに1つ進むナビゲーションのテキスト |
| start | Number | 1  | 初期ロード時のタブ開始位置 |
| position | String | 'bottom'  |  	ページナビゲーションの表示位置<br />（ 'top' または 'bottom' を指定可能） |
| scroll | Boolean | true  |  	スクロール位置を保持<br />（ true または false を指定可能） |

## Example

``` html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title>jQuery TabPager Plugin</title>
    <link href="css/jquery.tabpager.css" rel="stylesheet">
    <style>
      /* スタイルはこんな感じで上書可能 */
      .jquery-tab-pager-tabbar  li.current {
        color: #fff;
      }
      #tab li.current {
        font-style: italic;
      }
      #jquery-tab-pager-navi {
        margin-bottom: 10px;
      }

      /* ここから独自スタイル */
      h1 { font-family: 'Helvetica Neue', Helvetica, sans-serif; }
      #wrapper {
        border: 1px solid #eee;
        padding: 10px;
      }
      .contents {
        margin-bottom: 10px;
      }
    </style>
    <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="js/jquery.tabpager.js"></script>
    <script>
      $(document).ready(function()
      {
        /**
         * @param items		1ページあたりの最大表示数（省略時の初期値は 5 ）
         * @param contents	タブコンテンツのクラス名（省略時の初期値は 'contents' ）
         * @param time		ページ切り替え時のフェードイン時間（省略時の初期値は 800 ）
         * @param previous	前のページに1つ戻るナビゲーションのテキスト（省略時の初期値は 'Previous&raquo;' ）
         * @param next		次のページに1つ進むナビゲーションのテキスト（省略時の初期値は '&laquo;Next' ）
         * @param start		初期ロード時のタブ開始位置（省略時の初期値は 1 ）
         * @param position	ページナビゲーションの表示位置（ 'top' または 'bottom' を指定可能で省略時の初期値は 'bottom' ）
         * @param scroll	スクロール位置を保持（ true または false を指定可能で省略時の初期値は true ）
         */
        $("#tab").tabpager({
          items: 5,
          contents: 'contents',
          //time: 300,
          previous: '&laquo;前へ',
          next: '次へ&raquo;',
          //start: 1,
          position: 'top',
          //scroll: true
        });
      });
    </script>
  </head>
  <body>
    <h1>jQuery TabPager Plugin</h1>
    <ul id="tab">
      <li>TAB1</li>
      <li>TAB2</li>
      <li>TAB3</li>
      <li>TAB4</li>
    </ul>
    <div id="wrapper">
      <div class="contents">
        <div>contents1-1</div>
        <div>contents1-2</div>
        <div>contents1-3</div>
        <div>contents1-4</div>
        <div>contents1-5</div>
        <div>contents1-6</div>
        <div>contents1-7</div>
        <div>contents1-8</div>
        <div>contents1-9</div>
        <div>contents1-10</div>
        <div>contents1-11</div>
      </div>
      <div class="contents">
        <div>contents2-1</div>
        <div>contents2-2</div>
        <div>contents2-3</div>
        <div>contents2-4</div>
        <div>contents2-5</div>
        <div>contents2-6</div>
        <div>contents2-7</div>
        <div>contents2-8</div>
        <div>contents2-9</div>
        <div>contents2-10</div>
        <div>contents2-11</div>
      </div>
      <div class="contents">
        <div>contents3-1</div>
        <div>contents3-2</div>
        <div>contents3-3</div>
        <div>contents3-4</div>
        <div>contents3-5</div>
        <div>contents3-6</div>
        <div>contents3-7</div>
        <div>contents3-8</div>
        <div>contents3-9</div>
      </div>
      <div class="contents">
        <div>contents4-1</div>
      </div>
    </div>
  </body>
</html>
```

## For Developer
Node.jsおよびGulp.jsをインストールしてください。
```
cd build/ && npm install && gulp
```
