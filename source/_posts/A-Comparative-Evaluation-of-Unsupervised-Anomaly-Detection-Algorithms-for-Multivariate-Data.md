---
title: >-
  A-Comparative-Evaluation-of-Unsupervised-Anomaly-Detection-Algorithms-for-Multivariate-Data
date: 2018-06-21 09:29:51
tags:
- "論文要約"
- "異常検知"
---

## 1. どんなもの？
本論文では19の異なる教師なし異常検知の手法を10の異なるドメインのデータセットを用いて比較し、教師なし異常検知の指標を提示している。
それぞれの手法の強みと弱みやアルゴリズムのパフォーマンスや必要な計算リソース、パラメータチューニングといった特徴について言及し、
各シナリオに応じてどのようなアルゴリズムが効果的か提案している。
nearest-neighborベースのアルゴリズムが総合的に良い結果を
グローバル異常検知の場合はk-NN, ローカル異常検知の場合はLOFをクラスタリングベースアルゴリズムの代わりに使うと良い。
もし、データセットのサイズが大きく、計算時間が重視される場合、HBOSが良い。
{% asset_img Table6.PNG ’Recommendations for algorithm selection’ %}

## 2. 先行研究と比べてどこがすごいの？
教師なし異常検知には様々な手法があるが、共通的に評価、比較した評価がない。
本論文では19のアルゴリズムを公平に評価し、教師なし異常検知の新たな指標を提示した。

## 3. 技術や手法の"キモ"はどこにある？


## 4. どうやって有効だと検証した？
10個の異なるドメインのデータセットを用いて、各アルゴリズムを公平に評価した。

## 5. 議論はあるか？


## 6. 次に読むべき論文はあるか？


### 論文情報・リンク
* Markus Goldstein, Seiichi Uchida，"Robust, Deep and Inductive Anomaly Detection" PLoS ONE 11(4), 2016年 [論文リンク](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0152173)



- Local異常かGlobal異常のどちらかを検出したいかわからない場合はGlobal異常検知のアルゴリズムでとりあえず検証するのが良い。（そのほうが精度は出やすい）
- Clustringベースのアルゴリズムに比べ、Nearest-neighborベースのアルゴリズムの方がほとんどの場合精度が高い結果となった。計算リソースが限られている場合を除き、Nearest-neighborベースのアルゴリズムを使用する方が良い。
- Nearest-neighborベースの中ではk-NNが安定した精度が出ていた。
- ClusteringベースアルゴリズムはNearest-neighborに比べ、高速。
- uCBLOFやCMGOS-Regも比較的高速である。
- 特徴量の相関を考慮しないように思えるHBOSが良い結果を残した。（１０つのデータセットのうち、４つで最高の精度）
