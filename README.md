# 『医療診断支援AI開発　第1巻　入門編 ― 動かして、自分で作る』 ― コードとノートブック

書籍『**医療診断支援AI開発　第1巻　入門編 ― 動かして、自分で作る**』（『医療診断支援AI開発』全2巻の第1巻　入門編）のノートブックとコードを置いています。

**紙面のコードは「読んで理解するため」のもの、ここのノートブックは「動かすため」のものです。**
紙面から書き写したり、電子版から貼り付けたりすると、行の折り返しや記号の変換で崩れることがあります。
動かすときは、必ずここから取得してください。

---

## この巻の位置づけ

AIを**使い**、そして**作る** ― 第I部（第1〜12章）はブラウザだけで動く環境で医療画像AIを実際に動かし、第II〜IV部（第13〜40章）はその仕組みを理解して自分の手で書けるところまで。第1〜40章。

## ディレクトリ

```
book-vol1/
├── notebooks/          ← 章ごとのノートブック（chNN_*.ipynb）
│   ├── ch03_colab_basics.ipynb
│   ├── ch10_oct_classification.ipynb   ← 第I部のOCT画像分類の実習
│   ├── ch16_pytorch_basics.ipynb
│   ├── ch25_classification_e2e.ipynb   ← 分類の実装ガイド
│   └── ...
├── code/               ← 章をまたいで使う共通コード（Dataset、損失関数、評価指標など）
│   ├── datasets.py
│   ├── losses.py
│   └── metrics.py
├── tests/              ← code/ の単体テスト（臨床ロジックを守る）
├── requirements.txt    ← ライブラリのバージョン固定
├── data/               ← 公開データの入手先だけ（データ本体は置かない）
├── README.md           ← 使い方（まずここを読む）
└── errata.md           ← 正誤表・更新情報
```

本の各章の冒頭に「**この章のコード**」として、その章のノートブックのファイル名を記載しています。

## 章ごとのノートブック

「Open in Colab」のバッジを押すと、そのノートブックが Google Colab で開きます（Google アカウントが要ります）。ノートブックの中は、本文の節の見出しの順に、紙面のコードが並んでいます。

| 章 | 題 | ノートブック | Colab で開く |
|---|---|---|---|
| 第3章 | 環境構築なしで始める：Google Colab と Jupyter Notebook | [`notebooks/ch03_colab_basics.ipynb`](notebooks/ch03_colab_basics.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch03_colab_basics.ipynb) |
| 第4章 | データを用意する：公開データとアノテーションの基礎 | [`notebooks/ch04_code.ipynb`](notebooks/ch04_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch04_code.ipynb) |
| 第5章 | 代表的なモデルを使う：YOLO・nnU-Net・EfficientNet | [`notebooks/ch05_code.ipynb`](notebooks/ch05_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch05_code.ipynb) |
| 第6章 | 結果を確かめる：評価指標の基礎 | [`notebooks/ch06_code.ipynb`](notebooks/ch06_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch06_code.ipynb) |
| 第7章 | コードを共有する：GitHub入門 | [`notebooks/ch07_code.ipynb`](notebooks/ch07_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch07_code.ipynb) |
| 第8章 | 領域ごとに試す：眼科・整形外科・脳神経・消化器の最小限の実装例 | [`notebooks/ch08_code.ipynb`](notebooks/ch08_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch08_code.ipynb) |
| 第10章 | OCT画像分類の実習：データの入手から誤り分析まで | [`notebooks/ch10_oct_classification.ipynb`](notebooks/ch10_oct_classification.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch10_oct_classification.ipynb) |
| 第11章 | 自分の施設の画像で試す：持ち出し、匿名化、データの整え方 | [`notebooks/ch11_code.ipynb`](notebooks/ch11_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch11_code.ipynb) |
| 第13章 | Pythonの基礎 | [`notebooks/ch13_code.ipynb`](notebooks/ch13_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch13_code.ipynb) |
| 第14章 | 科学計算とデータ処理：NumPy・pandas・matplotlib | [`notebooks/ch14_code.ipynb`](notebooks/ch14_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch14_code.ipynb) |
| 第15章 | 医療AIの主要ライブラリ：画像の入出力から学習・評価まで | [`notebooks/ch15_code.ipynb`](notebooks/ch15_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch15_code.ipynb) |
| 第16章 | PyTorchの基礎 | [`notebooks/ch16_pytorch_basics.ipynb`](notebooks/ch16_pytorch_basics.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch16_pytorch_basics.ipynb) |
| 第17章 | 学習の仕組み：損失関数・最適化・評価 | [`notebooks/ch17_code.ipynb`](notebooks/ch17_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch17_code.ipynb) |
| 第18章 | 機械学習のさまざまな学習方式と利用方法：教師あり・強化・ゼロショット | [`notebooks/ch18_code.ipynb`](notebooks/ch18_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch18_code.ipynb) |
| 第19章 | 医療画像の基礎：DICOM、NIfTI、前処理 | [`notebooks/ch19_code.ipynb`](notebooks/ch19_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch19_code.ipynb) |
| 第20章 | 医療画像の座標系と位置合わせ：経過比較とマルチモダリティ | [`notebooks/ch20_code.ipynb`](notebooks/ch20_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch20_code.ipynb) |
| 第22章 | 検出：病変の位置を枠で示す | [`notebooks/ch22_code.ipynb`](notebooks/ch22_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch22_code.ipynb) |
| 第23章 | セグメンテーションとnnU-Net：病変の領域を画素単位で抽出する | [`notebooks/ch23_code.ipynb`](notebooks/ch23_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch23_code.ipynb) |
| 第24章 | 診断・分類とEfficientNet・Transformer：画像にラベルを与える | [`notebooks/ch24_code.ipynb`](notebooks/ch24_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch24_code.ipynb) |
| 第25章 | 実装ガイド（分類）：EfficientNetで最初から最後まで作る | [`notebooks/ch25_classification_e2e.ipynb`](notebooks/ch25_classification_e2e.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch25_classification_e2e.ipynb) |
| 第26章 | 実装ガイド（検出）：YOLOで病変を見つける | [`notebooks/ch26_code.ipynb`](notebooks/ch26_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch26_code.ipynb) |
| 第27章 | 実装ガイド（セグメンテーション）：MONAIで3次元画像から領域を抽出する | [`notebooks/ch27_code.ipynb`](notebooks/ch27_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch27_code.ipynb) |
| 第28章 | 学習の高速化と大規模化：混合精度・勾配累積・複数GPU | [`notebooks/ch28_code.ipynb`](notebooks/ch28_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch28_code.ipynb) |
| 第29章 | モダリティ別の前処理：CT・MRI・眼底写真・X線 | [`notebooks/ch29_code.ipynb`](notebooks/ch29_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch29_code.ipynb) |
| 第31章 | 評価指標をコードで実装する | [`notebooks/ch31_code.ipynb`](notebooks/ch31_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch31_code.ipynb) |
| 第32章 | データ管理の実装：対応表とパイプライン | [`notebooks/ch32_code.ipynb`](notebooks/ch32_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch32_code.ipynb) |
| 第33章 | 可視化の実装：オーバーレイと結果提示 | [`notebooks/ch33_code.ipynb`](notebooks/ch33_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch33_code.ipynb) |
| 第34章 | 学習ループを実装する：最良モデルの保存・再開・記録 | [`notebooks/ch34_code.ipynb`](notebooks/ch34_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch34_code.ipynb) |
| 第35章 | データの読み込みを実装する：DICOM・NIfTI・3次元画像 | [`notebooks/ch35_code.ipynb`](notebooks/ch35_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch35_code.ipynb) |
| 第36章 | 推論パイプラインを組む：入力から結果出力まで | [`notebooks/ch36_code.ipynb`](notebooks/ch36_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch36_code.ipynb) |
| 第37章 | データ拡張を実装する：2次元と3次元 | [`notebooks/ch37_code.ipynb`](notebooks/ch37_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch37_code.ipynb) |
| 第38章 | 損失関数を実装する：医療タスクに合わせて設計する | [`notebooks/ch38_code.ipynb`](notebooks/ch38_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch38_code.ipynb) |
| 第39章 | アンサンブルとTTAを実装する：複数の予測を統合する | [`notebooks/ch39_code.ipynb`](notebooks/ch39_code.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kewel-corp/book-vol1/blob/main/notebooks/ch39_code.ipynb) |

## 使い方

ノートブックは **Google Colab だけで完結します**。環境構築は不要です。

1. 上の「章ごとのノートブック」の一覧で、使う章の「Open in Colab」のバッジを押す（ノートブックの先頭にも同じバッジがあります）
2. ランタイムのタイプを **GPU** に変更する
3. セルを上から順に実行する

手元のマシンで動かす場合：

```bash
git clone https://github.com/kewel-corp/book-vol1.git
cd book-vol1
```

## 書籍の版とタグ

**お手元の本の冒頭の「サポートページ」の節に書かれているタグを使ってください。**

そのタグの版が、お手元の本の紙面と一字一句同じコードです。リポジトリの main は、刊行後の訂正やライブラリの仕様変更への追随を含む最新の版です。

| タグ | 対応する本 |
|---|---|
| `v1.1-book-release` | 2026年11月25日以降の版の本（サポートページの節に `v1.1-book-release` と書かれている本） |
| `v1.0-book-release` | 2026年11月の最初の版の本（サポートページの節に `v1.0-book-release` と書かれている本） |

タグの版を手元に取るには：

```bash
git checkout <タグ>
```

タグの版を Colab で開くには、上の一覧の Colab のリンクの `blob/main/` を `blob/<タグ>/` に替えます。

---

## 守っていただきたい一線

**患者データを、このリポジトリに置かないでください。**

Gitの履歴は消えません。一度コミットすると、削除して再コミットしても過去の版から取り出せます
（入門編 第7章）。`.gitignore` で DICOM・NIfTI・配列形式を機械的に締め出していますが、
最後に効くのは運用です。

Colab に載せてよいのは、**公開データセットと、自分で作った合成データだけ**です。
自施設のデータを扱う段取り（倫理審査 → 匿名化 → シリーズ選択 → ラベル定義 → 対応表）は、
入門編 第11章で扱っています。

## データについて

**このリポジトリにデータは含まれていません。** `data/README.md` に、
本書で使用する公開データセットの入手先と、それぞれの利用条件をまとめています。

**ライセンスと品質は別問題です。** 商用利用可であることは、そのまま学習に投入してよいという
意味ではありません。使う前に、自分の目で中身を確かめてください（応用編の眼底写真の章）。

## ライセンス

| 対象 | ライセンス |
|------|------------|
| コード・ノートブック（`notebooks/` 以下） | [MIT](LICENSE-CODE) |
| 書籍の文章・図版 | © 2026 庄納　崇. 無断転載・再配布を禁じます |

なお、ノートブックが利用する外部ライブラリのライセンスは、それぞれに従います。
とくに **YOLO（Ultralytics）は AGPL-3.0** で、学習済みの重みにも及ぶとされています。
商用製品や医療機器プログラム（SaMD）に載せる場合は、遵守するか商用ライセンスを確認してください
（入門編 第5章）。

## 不具合・ご質問

Issues でお知らせください。ライブラリの仕様変更でノートブックが動かなくなった場合も、
同様にご報告いただけると助かります。

## 免責

本リポジトリのコードおよび書籍に記載された技術情報は、**教育・研究を目的としたもの**です。
実際の診療への応用や医療機器としての実装にあたっては、薬機法をはじめとする関連法規、
および各医療機関の倫理規定に必ず従ってください。ここで扱うAIモデルは、いずれも医師の診断を
**支援**するものであり、医師の判断に代わるものではありません。
