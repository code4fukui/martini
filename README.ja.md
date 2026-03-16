# MARTINI

MARTINI(マーティーニ)は、Mapboxが開発したリアルタイムのテレインメッシュ生成用のJavaScriptライブラリです。

## デモ
[こちらのインタラクティブなObservableノートブック](https://observablehq.com/@mourner/martin-real-time-rtin-terrain-mesh)で、MARTINIのアルゴリズムの動作を確認できます。

## 機能
- 高さデータから、迅速に三角形メッシュを生成します
- レベルオブディテールの異なるメッシュを階層的に生成します

## 使い方
NPMからインストールして使用できます:

```bash
npm install @mapbox/martini
```

サンプルコード:

```js
// 257x257のグリッドサイズを持つメッシュ生成器を作成
const martini = new Martini(257);

// テレインデータ(長さ257^2の配列)からRTINヒエラルシーを生成
const tile = martini.createTile(terrain);

// 10m以下の誤差のメッシュを取得
const mesh = tile.getMesh(10);
```

## ライセンス
ISCライセンスです。