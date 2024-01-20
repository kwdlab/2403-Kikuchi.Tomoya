# 2403-Kikuchi.Tomoya

## Overview
モデル検査ツールVerifpal [1]を用いてQUIC [2]ハンドシェイクプロトコルのセキュリティ分析を行った。

## Description
Zhangらは、研究においてQUICのハンドシェイクプロトコルをモデル化し、セキュリティ検証と分析を暗号プロトコルのモデル検査ツールVerifpalを用いて行った[3]。検証に使用されたモデルについて、安全性を保ったまま高速化を図る方法について検討した結果、デジタル署名の処理に着目した。以下の表にまとめた四つのプロトコルを実装して安全性や実行時間を検証した。また、クエリの計算によってプロトコルの安全性を検証しているためクエリの有無についても併せて確認する。

| プロトコル番号 | 説明                               |
| -------------- | ---------------------------------- |
| プロトコル0    | 元のソースコード                   |
| プロトコル1    | デジタル署名の処理を後にしたもの   |
| プロトコル2    | デジタル署名の処理を除いたもの               |
| プロトコル3    | 直前でエラーを起こして処理が実行されなかったもの |


## Requirement
Verifpal v0.27.2.


## Usage

### Verifpal

```
$ verifpal verify [file_name].vp
```


## References

- [[1] Verifpal User Manual](https://verifpal.com/res/pdf/manual.pdf)
- [[2] IETF, RFC 9000](https://datatracker.ietf.org/doc/html/rfc9000)
- [[3] J. Zhang, L. Yang, X. Gao, G. Tang, J. Zhang and Q. Wang, "Formal Analysis of QUIC Handshake Protocol Using Symbolic Model Checking," 2021](https://ieeexplore.ieee.org/document/9328313)

## Author
- [tom018](https://github.com/tom018)

## License
GPL-3.0 license
