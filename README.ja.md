# Map Application

CSVデータからインタラクティブなマップ上に場所を表示する `<csv-map>` Webコンポーネントのデモ用シンプルなWebページです。

## デモ

- **[ライブデモ](https://code4fukui.github.io/map/)**
- [ブログ記事 (日本語)](https://fukuno.jig.jp/3277)

## 機能

- **使いやすさ**: `<csv-map>` HTMLタグを追加するだけでマップを表示します。
- **CSVベース**: インラインのCSVデータから直接マップマーカーを配置します。
- **インタラクティブなポップアップ**: マーカーをクリックすると、場所の詳細（名前、写真、リンク）を表示します。
- **Geo3x3対応**: 正確な位置情報のエンコードに [geo3x3](https://github.com/code4fukui/geo3x3-js) 形式を使用します。

## 使い方

HTMLページにマップを追加するには、以下の2つのステップを実行します。

1.  **スクリプトの読み込み**
    HTMLファイルの `<head>` に `csv-map.js` モジュールを追加します。

    ```html
    <script type="module" src="https://code4fukui.github.io/csv-map/csv-map.js"></script>
    ```

2.  **`<csv-map>` 要素の追加**
    `<body>` 内に `<csv-map>` 要素を配置し、CSV形式で場所データを記述します。1行目はヘッダーである必要があります。

    ```html
    <csv-map>
    name,url,geo3x3,photo
    Yokogawa Bunten,https://volga-rice.jimdofree.com/,,volga-yokogawa.jpg
    Sun Dome Fukui,http://www.sankan.jp/sundome/,E9138732236,
    Fukui National College of Technology,https://www.fukui-nct.ac.jp/,E9138732251953,
    </csv-map>
    ```

### CSVフォーマット

このコンポーネントは、ヘッダー行とそれに続く各場所のデータ行を必要とします。

-   `name`: (必須) 場所の名前。ポップアップに表示されます。
-   `url`: (任意) ポップアップからリンクするURL。
-   `geo3x3`: (必須) `geo3x3` 形式の位置座標。`geo3x3` の値がない行はマップ上に表示されません。
-   `photo`: (任意) 場所の画像のURLまたは相対パス。

## ライセンス

本プロジェクトは [MIT License](LICENSE) のもとで利用可能です。
