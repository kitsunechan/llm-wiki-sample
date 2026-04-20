# Integral circulant graphs

## メタデータ

- 出典: Wasin So, "Integral circulant graphs", Discrete Mathematics 306(1) (2006), 153-158.
- DOI: https://doi.org/10.1016/j.disc.2005.11.006
- PII: S0012365X05005832
- 元URL: https://www.sciencedirect.com/science/article/pii/S0012365X05005832
- 取得日: 2026-04-18.
- バージョン: Discrete Mathematics 306(1), 2006-01-28, pp. 153-158。ScienceDirect Open archive 版。
- 参照方法: DOI と ScienceDirect 記事ページを一次参照として使う。安定した DOI と PII があるため、snapshot は保存しない。

## 要約

この短報は、[[concepts/integral-circulant-graphs|integral circulant graph]] を特徴づける基本論文である。circulant graph は巡回群 $\mathbb{Z}_n$ 上の Cayley graph と見なせる。論文は、circulant graph $G(n; S)$ が整数スペクトルを持つための必要十分条件を、接続集合 $S$ が $\gcd(k, n)$ の値で決まる層の和集合になっていることとして与える。

この特徴づけにより、integral circulant graph は $n$ の真の約数集合 $D$ によって $ICG_n(D)$ と記述できる。後続文献ではこのクラスは gcd-graph とも呼ばれる。論文はまた、$n$ 頂点の非同型 integral circulant graph がちょうど $2^{\tau(n)-1}$ 個あるという予想を提示する。ここで $\tau(n)$ は $n$ の正の約数の個数である。この個数予想は、後の [[sources/automorphism-groups-of-rational-circulant-graphs|Automorphism Groups of Rational Circulant Graphs]] で有理 circulant graph の同型分類として解決されたと見なせる。

## 要点

- circulant graph は、巡回群 $\mathbb{Z}_n$ 上の Cayley graph であり、頂点 $i$ は $i+s$、$s \in S$ と隣接する。
- 無向単純グラフとして扱うには、$0 \notin S$ かつ $S = -S$ が必要である。
- $G_n(d) = \{ k : \gcd(k, n) = d,\ 1 \le k \le n-1 \}$ と置くと、$G(n; S)$ が integral circulant graph であることは、ある $n$ の真の約数集合 $D$ について $S = \bigcup_{d \in D} G_n(d)$ と書けることと同値である。
- したがって integral circulant graph は、頂点数 $n$ と真の約数集合 $D$ によって $ICG_n(D)$ と表せる。
- このクラスは後続研究で gcd-graph とも呼ばれる。
- 接続集合を約数の層に分けるため、同じ $\gcd(k, n)$ を持つ差分は同じ扱いになる。
- ループなしの integral circulant graph を定める接続集合は、真の約数の部分集合に対応するため $2^{\tau(n)-1}$ 個ある。
- 論文は、これらが非同型としても $2^{\tau(n)-1}$ 個になると予想した。後続の rational circulant graph の研究では、この非同型性が示されている。

## 関連ページ

- [[concepts/integral-circulant-graphs|integral circulant graph]]
- [[concepts/rational-circulant-graphs|有理 circulant graph]]
- [[concepts/integral-graphs|整数グラフ]]
