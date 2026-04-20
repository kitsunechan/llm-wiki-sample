# グラフ理論マップ

このマップは、グラフ理論の主要な概念群を、代数的・スペクトル的側面、彩色と再構成、極値・ランダム構造、有向グラフ、位相的グラフ、無限グラフに分けて整理する概念地図です。個別資料の読む順序ではなく、概念の包含、特殊例、道具、隣接領域を整理します。

## 中心概念

- [[concepts/integral-graphs|整数グラフ]] - 隣接行列の固有値がすべて整数であるグラフ。
- [[concepts/algebraic-degree-of-graphs|グラフの代数次数]] - 隣接固有値の splitting field が $\mathbb{Q}$ 上どれだけ大きいかを測る不変量。
- [[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] - 群と生成集合から作るグラフの固有値を表現論で見る枠組み。
- [[concepts/expander-graphs|エクスパンダーグラフ]] - 疎さと強い連結性を同時に満たすグラフ族。
- [[concepts/ramanujan-graphs|Ramanujan graph]] - 正則グラフの非自明固有値を最適境界に抑える強いスペクトル的エクスパンダー。
- [[concepts/vertex-transitive-graphs|頂点推移グラフ]] - 自己同型群が頂点集合へ推移的に作用する対称性の高いグラフ。
- グラフ不変量 - 木幅、パス幅、距離次元、距離スペクトル、彩色数、グラフエネルギー、局所密度など、グラフを比較・分類する量。
- Lovász 数・Shannon capacity・強積 - 情報理論由来のグラフ不変量と、グラフ積・固有値評価の交差。
- 極値・ランダム構造 - Ramsey 型問題、Turan 型問題、Mantel 型問題、ランダムグラフ、ランダムハイパーグラフ。

## 概念構造

### 代数的・スペクトル的グラフ理論

- [[concepts/integral-graphs|整数グラフ]]
  - [[concepts/algebraic-degree-of-graphs|グラフの代数次数]] - 整数グラフを代数次数1の特殊例として含む一般化。
  - [[concepts/counting-integral-graphs|整数グラフの個数]] - 整数グラフが全グラフの中でどれほど少ないかを問う。
  - [[concepts/integral-circulant-graphs|integral circulant グラフ]] - circulant グラフに制限した整数グラフ。
    - [[concepts/sos-conjecture-for-integral-circulant-graphs|So の予想]] - integral circulant グラフがスペクトルによって接続集合まで決まるかを問う。
    - [[concepts/rational-circulant-graphs|有理 circulant グラフ]] - 無向単純な circulant グラフでは integral circulant グラフと同じ対象として扱える。
    - [[concepts/integral-mixed-circulant-graphs|integral mixed circulant グラフ]] - 混合グラフのエルミート隣接スペクトルで整数性を見る拡張。
    - [[concepts/unitary-cayley-graphs|ユニタリケイリーグラフ]] - $D = \{1\}$ に対応する基本的な integral circulant グラフ。
    - [[concepts/isospectral-circulant-graphs|isospectral circulant グラフ]] - 異なる接続集合が同じ隣接スペクトルを生むかを問う隣接問題。
    - 自己同型群・kernel・geometric kernel - 約数集合がグラフ対称性や隣接行列の核へどう現れるかを見る方向。
    - 強正則・少数固有値・Ramanujan 性 - integral circulant グラフをスペクトル制約でさらに細分する方向。
  - [[concepts/graph-energy|グラフエネルギー]] - 固有値の絶対値和。整数スペクトルや数論的固有値計算と結びつく。
- グラフ特性多項式 - 隣接行列の特性多項式から固有値を計算し、部分グラフやグラフ演算とスペクトルを結びつける基本道具。
- [[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]]
  - [[concepts/schur-rings|Schur 環]] - 有理 circulant グラフの接続集合と自己同型群を整理する代数的道具。
  - [[concepts/circulant-graph-isomorphism-problem|circulant グラフ同型問題]] - 巡回群上のケイリーグラフがいつ同型になるかを判定する問題。
  - [[concepts/vertex-transitive-graphs|頂点推移グラフ]] - ケイリーグラフを含む、自己同型群が頂点に推移的に作用するグラフ類。
  - [[concepts/distance-regular-cayley-graphs|距離正則ケイリーグラフ]] - ケイリーグラフの群対称性と距離正則グラフの距離構造が交差する分類対象。
  - [[concepts/crested-products-of-markov-chains|マルコフ連鎖の crested product]] - 輪積、ゲルファント対、階層的なマルコフ連鎖のスペクトル解析と隣接する構成。
  - [[concepts/zig-zag-product|zig-zag product]] - ケイリーグラフの構成とエクスパンダー性に関わるグラフ積。
    - [[concepts/expander-cayley-graphs|エクスパンダー・ケイリーグラフ]] - 群と生成集合から得られるエクスパンダー性。
- [[concepts/expander-graphs|エクスパンダーグラフ]]
  - [[concepts/zig-zag-product|zig-zag product]] - 次数を制御しながら大きなエクスパンダーグラフを構成する道具。
  - [[concepts/expander-cayley-graphs|エクスパンダー・ケイリーグラフ]] - 群と生成集合から得られる対称性の高い特殊例。
  - [[concepts/ramanujan-graphs|Ramanujan graph]] - Alon-Boppana 型境界に達する強いスペクトル的エクスパンダー。
  - 固有値による拡大性判定 - 正則二部グラフの拡大性を第二固有値の分離で見る古典的導線。
  - Lovász 数・Ramanujan graph・Alon-Boppana bound - 正則グラフの極端な固有値制約を、情報理論的グラフ不変量とも接続する。

### 組合せデザインと列の自己相関

- [[concepts/convolution-numbers|畳み込み数]] - 巡回群上の二値列の自己相関ベクトルを数え、カタラン数・ナラヤナ数や Hadamard matrix の巡回構成と接続する。
- Hadamard matrix - 直交する $\pm 1$ 行をもつ行列で、巡回二値列の自己相関条件を通じて組合せデザインや符号理論と隣接する。
- 巡回自己相関 - 二値列の回転ずれごとの一致数を調べる道具で、circulant 行列を使う構成問題と結びつく。

### グラフ不変量と幅

- 木幅・パス幅 - 木分解やパス分解によって、グラフの木に近い構造を測る。
- 距離次元 - 距離ベクトルで頂点を識別するための基準点集合の最小サイズ。
- [[concepts/distance-spectra-of-graphs|距離スペクトル]] - 距離行列や Laplacian 距離行列など、隣接ではなく頂点間距離から作るスペクトル不変量。
- グラフエネルギー - [[concepts/graph-energy|グラフエネルギー]] は隣接行列の固有値の絶対値和で、スペクトル的グラフ理論と交差する。
- Lovász 数 - Shannon capacity の上界を与え、強積に対する振る舞いを通じて彩色数や固有値評価と交差する。
- グラフ密度 profile - 小さなグラフの密度ベクトルを用いて大域的な構造を測る。
- 次数列 - 頂点次数の分布や、同じ次数を持つ頂点の強制出現を通じてグラフを分類する。
- threshold graph と threshold dimension - 線形不等式や禁止誘導部分グラフで特徴づけられるグラフ類と、その交差表現に関する不変量。
- 距離正則グラフ - 距離ごとの近傍数が頂点対ではなく距離だけで決まる強い正則性を持つグラフ。ケイリーグラフに制限すると [[concepts/distance-regular-cayley-graphs|距離正則ケイリーグラフ]] の分類問題になる。

### 彩色と再構成

- グラフ彩色 - 頂点や辺へ色を割り当てる基本問題。彩色数、欠陥彩色、list coloring、対応彩色などへ分岐する。
- 再彩色 - 適切彩色の空間を、1 頂点ずつ色を変える遷移グラフとして見る。
- Kempe 同値 - Kempe chain による彩色間の到達可能性を扱う。
- 彩色対称関数 - グラフ彩色を対称関数として符号化し、$e$-positive 性などを問う。

### 極値・ランダム構造

- Ramsey 型問題 - 単色部分構造が避けられなくなる閾値を問う。
- Turan 型問題 - 禁止部分グラフや禁止ハイパーグラフのもとで、辺数やコピー数を最大化する。
- common graph と Ramsey multiplicity - 2辺彩色完全グラフにおける単色コピー数の最小化を、ランダム彩色や graphon 密度不等式と比較する。
- ランダムグラフ・ランダムハイパーグラフ - 疎ランダムグラフ、ランダム部分グラフ、半ランダム過程での閾値や構造を調べる。
- ハイパーグラフ - 辺が 3 頂点以上を含みうる一般化で、共次数閾値、完全マッチング、Hamiltonian 構造、spectral Turan 問題と結びつく。

### 有向グラフと分解

- 有向グラフ - 有向辺を持つグラフ。kernel、支配、arborescence、Oberwolfach 問題などを含む。
- rotor-routing model - 有向グラフ上で、各頂点の rotor の状態に従って粒子を移動させる力学系で、到達可能性や chip-firing と隣接する。
- 因子分解 - 辺集合を、マッチング、森、閉路、全域部分グラフなどの指定された部分グラフ族へ分解する。
- 行列木定理 - arborescence の数え上げや色制約付き構成の道具になる。

### 位相的・幾何的グラフ

- リボングラフ - 曲面上に埋め込まれたグラフを組合せ的に扱う対象。
- 部分双対 - リボングラフの一部の辺だけで双対化する操作で、Euler genus や minor 理論と関係する。
- グラフォン - 密グラフ列の極限を表す可測関数で、スペクトル、閉路密度、グラフ極限と結びつく。
- cospectral graphon - グラフォンのスペクトルや閉路密度が一致する関係で、有限グラフの cospectrality をグラフ極限へ拡張する。
- 超立方体グラフ - $n$ 次元超立方体の頂点と辺からなるグラフで、Hamming グラフ、距離正則性、Hamiltonian 構造、辺 slicing 問題と接続する。

### 無限グラフとポテンシャル論

  - [[concepts/lamplighter-graphs|lamplighter graph]] - wreath product やランダムウォークに現れるグラフ。
  - [[concepts/harmonic-functions-of-finite-energy|有限 Dirichlet energy の調和関数]] - lamplighter graph の解析的性質を記述する概念。

## 関係

- [[concepts/integral-circulant-graphs|integral circulant グラフ]] は、[[concepts/integral-graphs|整数グラフ]] と [[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] の交差に位置する。
- [[concepts/sos-conjecture-for-integral-circulant-graphs|So の予想]] は、integral circulant グラフの接続集合、スペクトル多重集合、同型性の関係を問う問題であり、[[concepts/isospectral-circulant-graphs|isospectral circulant グラフ]] の特殊で数論的な部分問題である。
- integral circulant グラフの強正則性、少数固有値、Ramanujan 性は、同じ Ramanujan sum 型のスペクトル計算に、異なるスペクトル制約を課した特殊化である。
- [[concepts/integral-mixed-circulant-graphs|integral mixed circulant グラフ]] は、integral circulant グラフを混合グラフへ拡張するが、整数性は通常の隣接行列ではなくエルミート隣接行列で定義される。
- [[concepts/algebraic-degree-of-graphs|グラフの代数次数]] は [[concepts/integral-graphs|整数グラフ]] を一般化し、[[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] の固有値がどの cyclotomic field の固定体に入るかを測る。
- [[concepts/rational-circulant-graphs|有理 circulant グラフ]] と [[concepts/schur-rings|Schur 環]] は、circulant グラフの分類と自己同型群をつなぐ。
- [[concepts/circulant-graph-isomorphism-problem|circulant グラフ同型問題]] は Ádám の予想、spectral Ádám property、Schur 環による同型判定を通じて、接続集合の同値関係を複数の強さで比較する。
- [[concepts/isospectral-circulant-graphs|isospectral circulant グラフ]] は、[[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] の指標和表示を使い、スペクトルが同型性をどこまで決めるかを巡回群上で問う。
- [[concepts/vertex-transitive-graphs|頂点推移グラフ]] は [[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] の上位的な対称性クラスであり、閉歩道数やスペクトル冪和の不変性を比較する場になる。
- [[concepts/distance-regular-cayley-graphs|距離正則ケイリーグラフ]] は、[[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] の指標和による解析と、距離正則グラフ・強正則グラフの分類問題を結びつける。
- [[concepts/crested-products-of-markov-chains|マルコフ連鎖の crested product]] は、[[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] と同じく作用素のスペクトルを見るが、群の生成集合よりも複数のマルコフ連鎖、テンソル積、階層構造から合成連鎖を作る点に特徴がある。
- [[concepts/unitary-cayley-graphs|ユニタリケイリーグラフ]] は、[[concepts/integral-circulant-graphs|integral circulant グラフ]] の特殊例であり、[[concepts/graph-energy|グラフエネルギー]] の計算対象になる。
- [[sources/some-properties-of-unitary-cayley-graphs|Some Properties of Unitary Cayley Graphs]] は、ユニタリケイリーグラフをグラフ不変量と整数スペクトルの両面から整理し、gcd-graph の整数性にもつなげる。
- [[concepts/expander-graphs|エクスパンダーグラフ]] は、スペクトル的グラフ理論、ランダムウォーク、誤り訂正符号、擬似乱数性をつなぐ隣接領域である。
- [[concepts/zig-zag-product|zig-zag product]] は、[[concepts/expander-graphs|エクスパンダーグラフ]] と [[concepts/expander-cayley-graphs|エクスパンダー・ケイリーグラフ]] の構成に関わる。
- [[concepts/lamplighter-graphs|lamplighter graph]] はケイリーグラフとして現れる一方で、[[concepts/harmonic-functions-of-finite-energy|有限 Dirichlet energy の調和関数]] のような無限グラフの解析概念とも結びつく。
- 木幅、距離次元、彩色数、グラフエネルギーは、いずれもグラフを数値的に比較する不変量だが、木幅は分解構造、距離次元は距離識別、彩色数は分割制約、グラフエネルギーはスペクトルを測る。
- Ramsey 型問題と Turan 型問題はどちらも極値的だが、Ramsey 型問題は色分けで避けられない単色構造を問う一方、Turan 型問題は禁じた部分構造のもとで最大化を問う。
- ハイパーグラフは、極値問題、ランダム構造、共次数条件、Hamiltonian 構造を通常のグラフから高次関係へ拡張する。
- 有向グラフは、支配、kernel、arborescence、分解問題を通じて、無向グラフとは異なる到達可能性と向き付けの制約を持つ。
- グラフォンは有限グラフを直接一般化した概念というより、密グラフ列の極限として、閉路密度やスペクトルの連続的な対応物を与える。
- [[concepts/convolution-numbers|畳み込み数]] は、グラフそのものの不変量ではないが、巡回群、circulant 行列、組合せデザイン、符号理論を介して代数的グラフ理論と隣接する。
- Lovász 数と Shannon capacity は、強積・独立数・彩色数・正則グラフの固有値評価をつなぎ、エクスパンダーや Ramanujan graph のスペクトル境界とも比較される。
- [[concepts/ramanujan-graphs|Ramanujan graph]] は [[concepts/expander-graphs|エクスパンダーグラフ]] の強いスペクトル的特殊例であり、ケイリーグラフ的な明示構成と正則グラフ一般の固有値下界をつなぐ。

## 根拠資料

- [[sources/a-survey-on-integral-graphs|A survey on integral graphs]]
- [[sources/graphs-with-integral-spectrum|Graphs with integral spectrum]]
- [[sources/computing-the-characteristic-polynomial-of-a-graph|Computing the Characteristic polynomial of a graph]]
- [[sources/integral-circulant-graphs|Integral circulant graphs]]
- [[sources/convolutions-of-ramanujan-sums-and-integral-circulant-graphs|Convolutions of Ramanujan Sums and Integral Circulant Graphs]]
- [[sources/new-results-on-the-energy-of-integral-circulant-graphs|New Results on the Energy of Integral Circulant Graphs]]
- [[sources/how-many-non-isospectral-integral-circulant-graphs-are-there|How many non-isospectral integral circulant graphs are there?]]
- [[sources/on-isospectral-integral-circulant-graphs|On Isospectral Integral Circulant Graphs]]
- [[sources/on-sos-conjecture-for-integral-circulant-graphs|On So's conjecture for integral circulant graphs]]
- [[sources/on-the-automorphism-group-of-integral-circulant-graphs|On the Automorphism Group of Integral Circulant Graphs]]
- [[sources/structural-properties-and-formulae-of-the-spectra-of-integral-circulant-graphs|Structural properties and formulae of the spectra of integral circulant graphs]]
- [[sources/on-the-kernel-of-integral-circulant-graphs|On the kernel of integral circulant graphs]]
- [[sources/the-geometric-kernel-of-integral-circulant-graphs|The Geometric Kernel of Integral Circulant Graphs]]
- [[sources/the-energy-of-integral-circulant-graphs-with-prime-power-order|The energy of integral circulant graphs with prime power order]]
- [[sources/a-determinant-involving-ramanujan-sums-and-sos-conjecture|A determinant involving Ramanujan sums and So's conjecture]]
- [[sources/sos-conjecture-for-integral-circulant-graphs-of-4-types|So's conjecture for integral circulant graphs of 4 types]]
- [[sources/characterization-of-strongly-regular-integral-circulant-graphs-by-spectral-approach|Characterization of strongly regular integral circulant graphs by spectral approach]]
- [[sources/integral-circulant-graphs-with-four-distinct-eigenvalues|Integral circulant graphs with four distinct eigenvalues]]
- [[sources/characterisation-of-all-integral-circulant-graphs-with-multiplicative-divisor-sets-and-few-eigenvalues|Characterisation of all integral circulant graphs with multiplicative divisor sets and few eigenvalues]]
- [[sources/integral-circulant-ramanujan-graphs-of-prime-power-order|Integral Circulant Ramanujan Graphs of Prime Power Order]]
- [[sources/integral-circulant-ramanujan-graphs-via-multiplicativity-and-ultrafriable-integers|Integral circulant Ramanujan graphs via multiplicativity and ultrafriable integers]]
- [[sources/circulants-and-their-connectivities|Circulants and their connectivities]]
- [[sources/integral-mixed-circulant-graph|Integral mixed circulant graph]]
- [[sources/constructions-of-isospectral-circulant-graphs|Constructions of isospectral circulant graphs]]
- [[sources/automorphism-groups-of-rational-circulant-graphs|Automorphism Groups of Rational Circulant Graphs]]
- [[sources/on-the-adam-conjecture-on-circulant-graphs|On the Ádám conjecture on circulant graphs]]
- [[sources/on-the-spectral-adam-property-for-circulant-graphs|On the spectral Ádám property for circulant graphs]]
- [[sources/the-existence-of-selfcomplementary-circulant-graphs|The existence of selfcomplementary circulant graphs]]
- [[sources/algebraic-degree-of-cayley-graphs-over-abelian-groups-and-dihedral-groups|Algebraic degree of Cayley graphs over abelian groups and dihedral groups]]
- [[sources/integral-cayley-graphs-over-finite-groups|Integral Cayley graphs over finite groups]]
- [[sources/spectra-of-cayley-graphs|Spectra of Cayley Graphs]]
- [[sources/eigenvalues-of-cayley-graphs|Eigenvalues of Cayley Graphs]]
- [[sources/the-spectrum-of-a-graph|The spectrum of a graph]]
- [[sources/on-the-walks-on-cayley-graphs|On the walks on Cayley graphs]]
- [[sources/on-the-number-of-closed-walks-in-vertex-transitive-graphs|On the number of closed walks in vertex-transitive graphs]]
- [[sources/on-the-distance-spectra-of-graphs|On the Distance Spectra of Graphs]]
- [[sources/fourier-analysis-on-distance-regular-cayley-graphs-over-abelian-groups|Fourier Analysis on Distance-Regular Cayley Graphs over Abelian Groups]]
- [[sources/on-the-structure-of-basic-sets-of-schur-rings-over-cyclic-groups|On the Structure of Basic Sets of Schur Rings over Cyclic Groups]]
- [[sources/the-isomorphism-problem-for-circulant-graphs-via-schur-ring-theory|The isomorphism problem for circulant graphs via Schur ring theory]]
- [[sources/the-schur-wielandt-theory-for-central-s-rings|The Schur-Wielandt Theory for Central S-Rings]]
- [[sources/on-cospectral-graphons|On Cospectral Graphons]]
- [[sources/some-properties-of-unitary-cayley-graphs|Some Properties of Unitary Cayley Graphs]]
- [[sources/the-energy-of-unitary-cayley-graphs|The energy of unitary cayley graphs]]
- [[sources/eigenvalues-and-expanders|Eigenvalues and Expanders]]
- [[sources/expander-graphs-and-their-applications|Expander graphs and their applications]]
- [[sources/ramanujan-graphs|Ramanujan graphs]]
- [[sources/ramanujan-diagrams|Ramanujan diagrams]]
- [[sources/tight-estimates-for-eigenvalues-of-regular-graphs|Tight Estimates for Eigenvalues of Regular Graphs]]
- [[sources/the-eigenvalues-of-random-symmetric-matrices|The eigenvalues of random symmetric matrices]]
- [[sources/entropy-waves-the-zig-zag-graph-product-and-new-constant-degree-expanders-and-extractors|Entropy Waves, the Zig-Zag Graph Product, and New Constant-Degree Expanders and Extractors]]
- [[sources/semi-direct-product-in-groups-and-zig-zag-product-in-graphs|Semi-direct product in groups and zig-zag product in graphs]]
- [[sources/on-graphs-groups-and-geometry|On Graphs, Groups and Geometry]]
- [[sources/observations-on-the-lovasz-theta-function-graph-capacity-eigenvalues-and-strong-products|Observations on the Lovász Theta-Function, Graph Capacity, Eigenvalues, and Strong Products]]
- [[sources/lamplighter-graphs-do-not-admit-harmonic-functions-of-finite-energy|Lamplighter graphs do not admit harmonic functions of finite energy]]
- [[sources/crested-products-of-markov-chains|Crested products of Markov chains]]
- [[sources/adams-conjecture-is-true-in-the-square-free-case|Ádám's conjecture is true in the square-free case]]
- [[sources/on-adams-conjecture-for-circulant-graphs|On Ádám's Conjecture for Circulant Graphs]]
- [[sources/a-solution-of-the-isomorphism-problem-for-circulant-graphs|A solution of the isomorphism problem for circulant graphs]]
- [[sources/isomorphism-problem-for-relational-structures-with-a-cyclic-automorphism|Isomorphism Problem for Relational Structures with a Cyclic Automorphism]]
- [[sources/integral-circulant-graphs-with-the-spectral-adam-property|Integral circulant graphs with the spectral Ádám property]]
- [[sources/ejc-volume-32-issues-1-4-graph-theory-papers|EJC Volume 32, Issues 1-4 のグラフ理論関連論文]]
- [[sources/ejc-volume-33-issue-1-graph-theory-papers|EJC Volume 33, Issue 1 のグラフ理論関連論文]]
- [[sources/ejc-volume-33-issue-2-graph-theory-papers|EJC Volume 33, Issue 2 のグラフ理論関連論文]]
- [[sources/arxiv-2026-04-18-graph-theory-screening|arXiv 2026-04-18 グラフ理論関連論文スクリーニング]]
- [[sources/convolution-numbers|Convolution numbers]]
