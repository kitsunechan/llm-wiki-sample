# ケイリーグラフのスペクトル

## 定義

有限群 $G$ と接続集合 $H \subset G$ から作るケイリーグラフ $\operatorname{Cay}(G, H)$ のスペクトルは、その隣接行列の固有値の多重集合である。ケイリーグラフは群の正則作用を自己同型として持つため、スペクトルは群の表現論と深く結びつく。

## 表現論による見方

Babai の論文 [[sources/spectra-of-cayley-graphs|Spectra of Cayley Graphs]] の基本的な見方は、ケイリーグラフの隣接行列を群代数の元による右乗法として見ることである。Liu と Zhou の [[sources/eigenvalues-of-cayley-graphs|Eigenvalues of Cayley Graphs]] は、この古典的な見方を含む既知結果と応用を、Cayley digraph や一般化されたケイリーグラフまで広げて整理するサーベイである。

Godsil, Holton, McKay の [[sources/the-spectrum-of-a-graph|The spectrum of a graph]] は、ケイリーグラフに限らないグラフスペクトルの古典的入口である。ケイリーグラフでは対称性により表現論が使えるが、一般のグラフスペクトルで何が同型や構造を反映するかを意識するための背景資料になる。

接続集合 $H$ に対応する群代数の元を $\sum_{h \in H} h$ と考えると、隣接行列はこの元で右から掛ける作用と対応する。群代数は既約表現に対応する成分へ分解できるので、隣接行列のスペクトルも既約表現ごとの情報へ分かれる。

## アーベル群の場合

$G$ がアーベル群の場合、既約表現はすべて1次元指標である。そのため固有値は非常に単純に、接続集合上の指標和として得られる。

$$
\lambda_\chi = \sum_{h \in H} \chi(h)
$$

この事実は、[[concepts/integral-circulant-graphs|integral circulant グラフ]] や [[concepts/rational-circulant-graphs|有理 circulant グラフ]] の理解にもつながる。巡回群 $\mathbb{Z}_n$ の場合、指標は根付き単位複素数で書けるため、固有値は接続集合に沿った根の和になる。接続集合が $\gcd(k, n)$ ごとの層の和集合になると、これらの和が整数になる。

[[sources/algebraic-degree-of-cayley-graphs-over-abelian-groups-and-dihedral-groups|Algebraic degree of Cayley graphs over abelian groups and dihedral groups]] は、この指標和を Galois 作用で解析し、アーベル群上のケイリーグラフ/digraph の splitting field と [[concepts/algebraic-degree-of-graphs|グラフの代数次数]] を完全に決定する。接続集合 $S$ を固定する $\mathbb{Z}_n^*$ の最大部分群 $H$ に対して、代数次数は $\varphi(n)/|H|$ になる。

接続集合が $\mathbb{Z}_n$ の単元全体である場合は [[concepts/unitary-cayley-graphs|ユニタリケイリーグラフ]] になり、固有値は Ramanujan sum として表される。この性質は グラフエネルギーの計算にも使われる。

[[sources/a-determinant-involving-ramanujan-sums-and-sos-conjecture|A determinant involving Ramanujan sums and So's conjecture]] は、$n$ の約数で添字付けた Ramanujan sum 行列の行列式を計算し、この行列が可逆であることを示す。この可逆性により、integral circulant グラフの接続集合から作られる順序付きスペクトルベクトルは、元の約数集合を決定する。

混合ケイリーグラフでは、接続集合が反転で閉じていないため、有向辺と無向辺が共存する。巡回群上の [[concepts/integral-mixed-circulant-graphs|integral mixed circulant グラフ]] では、エルミート隣接行列の固有値が、無向 circulant グラフの指標和と oriented circulant グラフの正弦型の指標和に分解される。この分解により、無向部分は So の integral circulant グラフの特徴づけへ、向き付け部分は $n \equiv 0 \pmod 4$ のときの $G_n^1(d)$ と $G_n^3(d)$ の層構造へ接続される。

## 非アーベル群の場合

非アーベル群では、既約表現が高次元になる。したがって、1つの既約指標から1個の固有値がただちに出るわけではない。Babai は、各既約指標に対応する固有値たちの冪和を指標で表し、それらの冪和から多項式を復元して固有値を得る方法を示す。

この枠組みは、通常の無向グラフだけでなく、複素数の色を持つ Cayley color graph に対して定式化されている。

[[sources/on-the-walks-on-cayley-graphs|On the walks on Cayley graphs]] は、ケイリーグラフ上の歩道数を隣接行列の冪や群の表示と結びつけて扱う。歩道数は固有値の冪和と対応するため、スペクトルを「閉歩道の数え上げ」として読む視点を補う。

## 頂点推移グラフとの比較

ケイリーグラフは群が頂点に正則に作用するため、必ず [[concepts/vertex-transitive-graphs|頂点推移グラフ]] である。ただし、頂点推移グラフがすべてケイリーグラフとは限らない。[[sources/on-the-number-of-closed-walks-in-vertex-transitive-graphs|On the number of closed walks in vertex-transitive graphs]] は、頂点推移グラフの閉歩道数を調べ、対称性がスペクトル的な量へどう反映されるかを見る補助資料になる。

## cospectral ケイリーグラフ

スペクトルが同じグラフを cospectral graph と呼ぶ。Babai は二面体群 $D_p$ 上のケイリーグラフを調べ、$p$ が十分大きい素数なら、任意の $k$ に対して $k$ 個の互いに非同型な cospectral ケイリーグラフが存在することを示した。

これは、ケイリーグラフのように対称性が強いグラフでも、スペクトルだけでは同型を判定できないことを示す。特に、巡回群上の integral circulant グラフでは接続集合とスペクトルが比較的制御しやすい一方、非アーベル群では事情がずっと複雑になる。

巡回群に制限した場合でも、スペクトルがグラフを一意に決めるわけではない。[[sources/constructions-of-isospectral-circulant-graphs|Constructions of isospectral circulant graphs]] は、circulant グラフの固有値が $n$ 乗根の和として表されることを使い、非自明な [[concepts/isospectral-circulant-graphs|isospectral circulant グラフ]] の構成を扱う。

[[sources/on-isospectral-integral-circulant-graphs|On Isospectral Integral Circulant Graphs]] は、この問いを integral circulant グラフに制限し、スペクトル一致が同型性を含意する integral spectral Ádám property を素因数分解型ごとに調べる。

グラフ同型そのものを問う場合は、[[concepts/circulant-graph-isomorphism-problem|circulant グラフ同型問題]] になる。Muzychuk の [[sources/a-solution-of-the-isomorphism-problem-for-circulant-graphs|A solution of the isomorphism problem for circulant graphs]] は、任意の位数の circulant グラフに対する同型判定基準を与える。スペクトル一致は同型の必要条件にすぎないため、isospectrality と同型判定は区別して扱う必要がある。

## expander と生成集合

ケイリーグラフのスペクトルは、[[concepts/expander-graphs|エクスパンダーグラフ]] や [[concepts/expander-cayley-graphs|エクスパンダー・ケイリーグラフ]] の判定にも関わる。正則グラフでは、最大固有値以外の固有値が十分小さいことが強い連結性や混合性を表すためである。

Alon, Lubotzky, Wigderson の論文 [[sources/semi-direct-product-in-groups-and-zig-zag-product-in-graphs|Semi-direct product in groups and zig-zag product in graphs]] は、半直積群のケイリーグラフと [[concepts/zig-zag-product|zig-zag product]] を結びつけ、ケイリーグラフの expander 性が群だけでなく生成集合に依存しうることを示した。

integral circulant グラフでは、Ramanujan graph の条件も約数集合と Ramanujan sum で解析できる。[[sources/integral-circulant-ramanujan-graphs-of-prime-power-order|Integral Circulant Ramanujan Graphs of Prime Power Order]] は素数冪位数で Ramanujan property を持つ integral circulant グラフを分類し、[[sources/integral-circulant-ramanujan-graphs-via-multiplicativity-and-ultrafriable-integers|Integral circulant Ramanujan graphs via multiplicativity and ultrafriable integers]] は乗法性を使ってより広い場合を扱う。

Lubotzky, Phillips, Sarnak の [[sources/ramanujan-graphs|Ramanujan graphs]] は、ケイリーグラフ的な代数構成で最適に近いスペクトルギャップを持つ正則グラフ族を作る古典的資料である。[[sources/ramanujan-diagrams|Ramanujan diagrams]] と [[sources/tight-estimates-for-eigenvalues-of-regular-graphs|Tight Estimates for Eigenvalues of Regular Graphs]] は、Ramanujan 境界と正則グラフの固有値評価を理解するための隣接資料になる。
