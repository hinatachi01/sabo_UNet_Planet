# 衛星画像と深層学習を活用した広域・多時期の斜面崩壊地分布図作成

## 概要 Overview
広域 (日本国内など) を対象とした斜面崩壊地分布図の作成のため、
複数の斜面崩壊事例を学習し、未学習の事例を予測するU-Netモデルの開発。

## 使用データ Data used
* 特徴量作成用: 衛星画像 (PlanetScope), 標高データ (基盤地図情報 数値標高モデル https://service.gsi.go.jp/kiban/)
* マスク作成用: 崩壊地判読図 (国土地理院 防災・災害対応 https://www.gsi.go.jp/bousai.html)

* 使用した事例:
** H29 九州北部豪雨 (福岡県赤谷川)
** H30 北海道胆振東部地震 (北海道胆振地方)
** R01 台風19号豪雨 (宮城県五福谷川)
** R06 能登半島地震 (石川県能登地方)
** R06 能登半島豪雨 (石川県能登地方)

※ 128 pixel x 128 pixelのタイルに切り取り (モデル入力形式)。
※ 崩壊地:非崩壊地の割合が2:8より偏っていないタイルのみを使用。

## モデルのパラメータ Model Specification
model無印: 
　学習の重みづけ: 
　
model_2:
　学習の重みづけ: 
 
## datasetディレクトリの構成
dataset
 - test
 - -  images
 - -  masks
 - val
 - -  images
 - -  masks
 - test
 - -  images
 - -  masks
