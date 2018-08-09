---
title: In-Defense-of-the-Triplet-Loss-for-Person-Re-Identification
date: 2018-07-10 18:52:47
tags:
- "画像認識"
- "ニューラルネットワーク"
- "顔認識"
---

## 1. どんなもの？
surogate lossに比べ、triplet lossは以下の点から有用でないというのが通説であった。
- データセットが大きくなればなるほど、取りうるtripletの数も３乗に増えていき、トレーニング時間が膨大になる
- そのため、hard tripletのminingが必要となるが、hardest tripletだけだと外れ値だけで学習することになってしまう。
- そこで一般的にはmoderate negativesやmoderate positivesをminingすることが多い。
どのようなminingをするにしても大きな塊を直近のfでembeddingし、それらのデータポイントの距離を取る必要がある。
上記に関して既存の方法には無駄があるため、本論文ではtriplet lossの既存の方法に変更を加え、提案している。
- Batch Hard
- Batch All

- データセット
MARS
Market-1501
CUHK03

- Model
TriNet ... batch hard triplet loss 
LuNet ... scratch

- Evaluation
mean average precision score (mAP)
cumulative matching curve (CMC) at rank-1, rank-5

Identification models
Verification models

## 2. 先行研究と比べてどこがすごいの？


## 3. 技術や手法の"キモ"はどこにある？


## 4. どうやって有効だと検証した？
学習済みネットワークと組み合わせ、３つのReIDデータセットを用いた。
顔認識において訓練済みネットワークを使うことが多かったが、スクラッチで作ったネットワークも高いスコアを出し、有効であることを示した。


## 5. 議論はあるか？


## 6. 次に読むべき論文はあるか？
- 評価方法

### 論文情報・リンク
* Hermans Alexander, Beyer Lucas, Leibe Bastian, "In Defense of the Triplet Loss for Person Re-Identification" 2017年 [論文リンク](http://arxiv.org/abs/1703.07737)
