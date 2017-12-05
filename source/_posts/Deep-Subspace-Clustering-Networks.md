---
title: Deep Subspace Clustering Networks
date: 2017-12-05 16:42:13
tags: 
- "論文要約"
- "クラスタリング"
- "教師なし学習"
---

## 1. どんなもの？
教師なし学習における部分空間クラスタリングのニューラルネットワークに関わる提案。
部分空間クラスタリングにおいて効果的と言われてきたself-expressivenessプロパティの代わりにencorderとdecoderの間にself-expressiveness層として代替する案を提案している。
また、部分空間クラスタリングを効果的に学習させる事前学習やfine-tuning方法も提案。
検証により本手法が部分空間クラスタリングより性能が優れていることを示している。

## 2. 先行研究と比べてどこがすごいの？
本提案を利用することで、backpropagationを通して全てのデータの関連性をシンプルで、効果的に導き出せる。
非線形であるため、複雑な構造にも適用可能。

## 3. 技術や手法の"キモ"はどこにある？
効果的と言われてきたself-expressivenessプロパティの代わりにencorderとdecoderの間にself-expressiveness層として代替するというアプローチ。

## 4. どうやって有効だと検証した？
部分空間クラスタリングにおいて人気のあるベンチマークデータセットであるThe Extended Yale B datasetを用いて検証。

## 5. 議論はあるか？

## 6. 次に読むべき論文はあるか？
- 部分空間クラスタリング（Subspace Clustering）について
[P. Ji, M. Salzmann, and H. Li. Efficient dense subspace clustering. In WACV, pages 461–468. IEEE, 2014.](http://ieeexplore.ieee.org/document/6836065/?reload=true)

### 論文情報・リンク

* Pan Ji, Tong Zhang, Hongdong Li, Mathieu Salzmann, Ian Reid (Poster)，"Deep Subspace Clustering Networks" NIPS Proceedingsβ，2017年 [論文リンク](http://papers.nips.cc/paper/6608-deep-subspace-clustering-networks)