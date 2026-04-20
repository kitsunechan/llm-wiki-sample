# Spectra of Cayley Graphs

## メタデータ

- 出典: Laszlo Babai, "Spectra of Cayley Graphs", Journal of Combinatorial Theory, Series B 27 (1979), 180-189.
- DOI: https://doi.org/10.1016/0095-8956(79)90079-0
- PII: 0095895679900790
- 元URL: https://www.sciencedirect.com/science/article/pii/0095895679900790
- 取得日: 2026-04-18.
- バージョン: Journal of Combinatorial Theory, Series B 27, 1979, pp. 180-189。
- 参照方法: DOI と ScienceDirect 記事ページを一次参照として使う。安定した DOI と PII があるため、snapshot は保存しない。

## 要約

この論文は、[[concepts/cayley-graph-spectra|Cayley graph のスペクトル]] を有限群の表現論、とくに既約指標を使って計算する古典的な論文である。Lovasz の結果により、頂点推移的な自己同型群を持つグラフのスペクトル問題は Cayley graph のスペクトル問題へ還元できる。Babai は Cayley color graph という少し一般化された枠組みで、スペクトルの冪和を既約指標で表し、そこから各既約表現に対応する固有値を復元する方法を与える。

論文はさらに、この公式を二面体群 $D_p$ の Cayley graph に適用し、$p$ が十分大きい素数のとき、互いに非同型だが同じスペクトルを持つ Cayley graph の大きな族を構成する。これは、Cayley graph の強い対称性があっても、スペクトルだけでは同型を判定できないことを示す例である。

## 要点

- Cayley graph の隣接行列は、群代数の元による右乗法作用として見られる。
- そのため、群代数を既約表現に対応する最小右加群へ分解することで、隣接行列のスペクトルを表現論に分解できる。
- アーベル群の場合は既約表現がすべて1次元なので、固有値は接続集合上の指標和として直接計算できる。
- 非アーベル群では既約表現の次元が1より大きくなるため、各既約指標に対応する複数の固有値を、冪和と Newton-Waring 型の恒等式から復元する。
- 二面体群 $D_n$ への応用では、接続集合のうち回転部分と反射部分がスペクトルにどう寄与するかを具体的に計算する。
- 論文は、十分大きい素数 $p$ に対して、$D_p$ の非同型な cospectral Cayley graph を任意個数構成できることを示す。
- これは、circulant graph、すなわち巡回群上の Cayley graph とは異なり、一般の非アーベル群上の Cayley graph ではスペクトルと同型の関係がかなり複雑になることを示している。

## 関連ページ

- [[concepts/cayley-graph-spectra|Cayley graph のスペクトル]]
- [[concepts/integral-circulant-graphs|integral circulant graph]]
- [[concepts/rational-circulant-graphs|有理 circulant graph]]
- [[concepts/schur-rings|Schur 環]]
