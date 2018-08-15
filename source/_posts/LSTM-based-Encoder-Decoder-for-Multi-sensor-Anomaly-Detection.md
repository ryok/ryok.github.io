---
title: LSTM-based-Encoder-Decoder-for-Multi-sensor-Anomaly-Detection
date: 2018-08-13 15:11:17
tags:
- "論文要約"
- "異常検知"
- "時系列"
---

## 1. どんなもの？
LSTMベースのEncoder, Decoderを利用した、複数センサーデータの異常検知に対応した異常検知手法の提案。
検証の結果以下の点で有用であることを示した。
- positive likelihood が1.0を大幅に上回り、高い異常検知スコアを示した。
- 周期的なデータに対して、複数のWindow枠でも異常検知した。
- predictable、nonpredictableなデータセット両方において、異常検知可能であることを示した。

## 2. 先行研究と比べてどこがすごいの？
既存手法としては以下。
- LSTMをprediction modelとして異常検知する
- Autoencoderの復元誤差を利用した異常検知
本手法では言語モデルのようにLSTMのEncoder, Decoderを利用することで、時系列データに対して復元誤差を利用した異常検知を適用した。

## 3. 技術や手法の"キモ"はどこにある？
Encoderでベクトル表現を取得し、Decoderで復元し、復元誤差を最適化する。
LSTMを利用することにより復元誤差を時系列データに対して適用できる。

## 4. どうやって有効だと検証した？
５種類のデータセットで検証。データセットはpredictableなものとnon predictableなものを含む。
全てにおいて高い異常検知スコアを示した。

## 5. 議論はあるか？
- EncDec-ADはpredictableなデータだけでなく、unpredictableなデータに対しても良い性能を示した。
そのため、他の手法と比べてもロバストであるかもしれない。ただし、他のモデルと公平に比較した訳ではないので、ちゃんとした比較が必要。
- ROCではなく、positive likelihood(TRP/FPR)で評価していたが、どちらが良いのか？

## 6. 次に読むべき論文はあるか？

### 論文情報・リンク
* Pankaj Malhotra, Anusha, "LSTM-based-Encoder-Decoder-for-Multi-sensor-Anomaly-Detection" 2016年 [論文リンク]()
