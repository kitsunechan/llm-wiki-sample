# integral circulant グラフ

## 定義

integral circulant グラフは、circulant グラフであり、かつ隣接行列の固有値がすべて整数であるグラフである。circulant グラフは巡回群 $\mathbb{Z}_n$ 上のケイリーグラフ $G(n; S)$ として表せる。頂点集合は $\mathbb{Z}_n = \{0, 1, \ldots, n-1\}$ で、頂点 $i$ は $i+s$、$s \in S$ と隣接する。

無向単純グラフとして考える場合、接続集合 $S$ は $0 \notin S$ かつ $S = -S$ を満たす。

## So の特徴づけ

Wasin So の論文 [[sources/integral-circulant-graphs|Integral circulant graphs]] は、circulant グラフが整数グラフになる条件を次の形で特徴づけた。

$$
G_n(d) = \{ k : \gcd(k, n) = d,\ 1 \le k \le n-1 \}
$$

と置く。このとき、circulant グラフ $G(n; S)$ が integral circulant グラフであることは、ある $n$ の真の約数集合 $D$ について

$$
S = \bigcup_{d \in D} G_n(d)
$$

と書けることと同値である。

このため、integral circulant グラフは頂点数 $n$ と真の約数集合 $D$ によって $ICG_n(D)$ と書ける。後続文献では、このクラスは gcd-graph とも呼ばれる。

## 有理 circulant グラフとの関係

隣接行列の特性多項式は整数係数で monic なので、固有値がすべて有理数なら実際には整数である。したがって、無向単純 circulant グラフの文脈では、[[concepts/rational-circulant-graphs|有理 circulant グラフ]] と integral circulant グラフは同じ対象を指す。

So の特徴づけは、後の有理 circulant グラフの Schur 環による整理と同じ現象をより直接的に述べている。接続集合が $\gcd(k, n)$ ごとの層の和集合になることは、$\mathbb{Z}_n$ の単元群が作る軌道に沿って接続集合が閉じていることを意味する。

## mixed circulant グラフへの拡張

[[concepts/integral-mixed-circulant-graphs|integral mixed circulant グラフ]] は、接続集合が反転で閉じていない場合も許して、有向辺と無向辺が共存する circulant グラフへ整数性の問いを拡張する。ここでの整数性は、通常の隣接行列ではなくエルミート隣接行列の固有値に対して定義される。

Kadyan と Bhattacharjya の [[sources/integral-mixed-circulant-graph|Integral mixed circulant graph]] は、無向部分には So の $\gcd(k,n)$ 層による特徴づけがそのまま効き、向き付け部分は $n \equiv 0 \pmod 4$ の場合にだけ非自明に現れることを示す。したがって integral mixed circulant グラフは、integral circulant グラフを含むが、頂点数が $4$ の倍数かどうかで振る舞いが大きく変わる。

## スペクトル計算との関係

circulant グラフはアーベル群 $\mathbb{Z}_n$ 上のケイリーグラフなので、[[concepts/cayley-graph-spectra|ケイリーグラフのスペクトル]] は1次元指標の和として計算できる。接続集合 $S$ に対して、固有値は $S$ 上で根付き単位複素数を足し合わせたものになる。So の特徴づけは、この指標和がすべて整数になる接続集合を、$\gcd(k, n)$ の層の和集合として分類している。

[[sources/convolutions-of-ramanujan-sums-and-integral-circulant-graphs|Convolutions of Ramanujan Sums and Integral Circulant Graphs]] は、A-convolution と Ramanujan sum を使い、乗法的約数集合を持つ integral circulant グラフの固有値とエネルギーを素因子ごとの構造へ分解する。

同じ指標和は、2つの circulant グラフが同じスペクトルを持つかを調べる [[concepts/isospectral-circulant-graphs|isospectral circulant グラフ]] の問題にも現れる。integral circulant グラフでは「指標和が整数になる条件」を問うのに対し、isospectral circulant グラフでは「異なる接続集合が同じ指標和の多重集合を生む条件」を問う。

## 個数

$n$ の正の約数の個数を $\tau(n)$ とする。ループを避けるには $d = n$ に対応する `0` を接続集合から除くため、真の約数の選び方は $2^{\tau(n)-1}$ 通りある。したがって、$n$ 頂点の integral circulant グラフを定める接続集合は $2^{\tau(n)-1}$ 個ある。

So は、非同型な integral circulant グラフの個数も $2^{\tau(n)-1}$ であると予想した。後続の [[sources/automorphism-groups-of-rational-circulant-graphs|Automorphism Groups of Rational Circulant Graphs]] は、有理 circulant グラフの同型類数が $2^{\tau(n)-1}$ であることを示しており、この予想を解決する結果として読める。

[[sources/on-the-automorphism-group-of-integral-circulant-graphs|On the Automorphism Group of Integral Circulant Graphs]] は、integral circulant グラフの自己同型群を直接扱い、約数集合が生む層構造と対称性を結びつける。この方向は、スペクトルで接続集合を復元する問題とは別に、同じ約数データがどれだけ大きなグラフ対称性を強制するかを見る入口になる。

## So の予想と Ramanujan sum 行列

[[concepts/sos-conjecture-for-integral-circulant-graphs|So の予想]] は、integral circulant グラフのスペクトルが頂点数 $n$ と接続集合を決定するかを問う。関連する性質として、[[sources/on-isospectral-integral-circulant-graphs|On Isospectral Integral Circulant Graphs]] は、同じスペクトルを持つ位数 $N$ の integral circulant グラフが同型になる条件を integral spectral Ádám property として扱う。固有値を順序付きベクトルとして見れば、接続集合 $S$ から

$$
\left(\sum_{d\in S} c(\ell,n/d)\right)_{\ell=1}^n
$$

が得られる。ここで $c(\ell,n/d)$ は Ramanujan sum である。

[[sources/a-determinant-involving-ramanujan-sums-and-sos-conjecture|A determinant involving Ramanujan sums and So's conjecture]] は、$n$ の約数で添字付けた Ramanujan sum 行列 $C_n=(c(d,t))_{d,t\in\mathcal{D}(n)}$ について

$$
\det C_n = \pm n^{\tau(n)/2}
$$

を示す。このため $C_n$ は可逆であり、順序付きスペクトルベクトルは約数集合 $S$ を決定する。これは、固有値の順序を忘れた多重集合が接続集合を決定するかという So の予想そのものより弱いが、スペクトル情報が接続集合をどの段階で失うかを切り分ける結果である。

同論文はさらに、Euler 関数値が十分に分離している $n$ では So の予想が成り立つこと、小さな素因子を持たないほとんどすべての整数でも成り立つことを示す。後続の [[sources/how-many-non-isospectral-integral-circulant-graphs-are-there|How many non-isospectral integral circulant graphs are there?]] と [[sources/sos-conjecture-for-integral-circulant-graphs-of-4-types|So's conjecture for integral circulant graphs of 4 types]] は、素因数分解の型を制限して So の予想を確認する部分結果を与える。

[[sources/structural-properties-and-formulae-of-the-spectra-of-integral-circulant-graphs|Structural properties and formulae of the spectra of integral circulant graphs]] は、固有値公式と構造的性質をさらに整理し、[[sources/on-the-kernel-of-integral-circulant-graphs|On the kernel of integral circulant graphs]] は隣接行列の kernel を調べる。これらは So の予想そのものの証明ではないが、スペクトルから見える不変量を増やすための補助資料になる。

## 強正則性と少数固有値

connected regular graph がちょうど3つの相異なる固有値を持つ場合、それは強正則グラフである。このため、integral circulant グラフの中で相異なる固有値が少ないものを分類する問題は、強正則グラフの分類と直結する。

[[sources/characterization-of-strongly-regular-integral-circulant-graphs-by-spectral-approach|Characterization of strongly regular integral circulant graphs by spectral approach]] は、connected $ICG_n(D)$ が強正則であることを、$n$ が合成数であり、ある $m \mid n$ について

$$
D = \{d \in D_n : m \nmid d\}
$$

と書けることとして特徴づける。

4個の相異なる固有値を持つ場合は、強正則グラフより少し広い regular graph の構造が現れる。[[sources/integral-circulant-graphs-with-four-distinct-eigenvalues|Integral circulant graphs with four distinct eigenvalues]] はその一部を扱い、[[sources/characterisation-of-all-integral-circulant-graphs-with-multiplicative-divisor-sets-and-few-eigenvalues|Characterisation of all integral circulant graphs with multiplicative divisor sets and few eigenvalues]] は、乗法的約数集合を仮定して、相異なる固有値が高々4個の場合を体系的に分類する。

## Ramanujan 性

integral circulant グラフは固有値を数論的に計算できるため、Ramanujan graph のような強いスペクトル制約を調べやすい。connected $\rho$-regular graph が Ramanujan であるとは、最大固有値以外の固有値の絶対値が $2\sqrt{\rho-1}$ 以下に抑えられることである。

[[sources/integral-circulant-ramanujan-graphs-of-prime-power-order|Integral Circulant Ramanujan Graphs of Prime Power Order]] は、素数冪位数 $p^s$ の $ICG(p^s,\mathcal{D})$ について Ramanujan property を持つものを完全に列挙する。[[sources/integral-circulant-ramanujan-graphs-via-multiplicativity-and-ultrafriable-integers|Integral circulant Ramanujan graphs via multiplicativity and ultrafriable integers]] は、約数集合の乗法性を使って複数の素因子を持つ場合へ進む。

## 幾何的 kernel と leaping set

[[sources/the-geometric-kernel-of-integral-circulant-graphs|The Geometric Kernel of Integral Circulant Graphs]] は、integral circulant グラフの geometric kernel を扱い、グラフの幾何的表示と約数集合の関係を調べる。Sander の一連の研究では leaping set のような数論的な補助集合も現れ、スペクトル公式だけではなく、頂点配置・kernel・約数構造を横断して同じクラスを理解する。

## 連結度

circulant グラフは通信ネットワークのモデルとしても研究され、連結度や辺連結度が重要になる。[[sources/circulants-and-their-connectivities|Circulants and their connectivities]] は、integral 条件に限らない一般の circulant グラフの連結度を扱う古典的資料である。スペクトルや整数性とは別に、頂点推移的なネットワークとしての頑健性を考える入口になる。

## 重要性

integral circulant グラフは、整数グラフの中でも明確に分類できる大きな部分クラスである。circulant グラフは通信ネットワークや分散計算のモデルとして現れ、さらに後続研究では quantum spin network の perfect state transfer とも結びつく。$D = \{1\}$ の場合は [[concepts/unitary-cayley-graphs|ユニタリケイリーグラフ]] であり、[[concepts/graph-energy|グラフエネルギー]] や hyperenergetic 条件も詳しく調べられている。

[[sources/new-results-on-the-energy-of-integral-circulant-graphs|New Results on the Energy of Integral Circulant Graphs]] は、このエネルギー研究をユニタリケイリーグラフから一般の integral circulant グラフへ広げる資料である。

素数冪位数に限ると、[[sources/the-energy-of-integral-circulant-graphs-with-prime-power-order|The energy of integral circulant graphs with prime power order]] がエネルギー計算を詳しく扱う。素因数分解の型を固定して公式を得るという点で、Ramanujan 性や So の予想の部分結果と同じ数論的分割の発想を共有する。
