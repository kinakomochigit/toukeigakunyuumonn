# [データ分析に必須の知識・考え方 統計学入門 仮説検定から統計モデリングまで重要トピックを完全網羅](https://www.socym.co.jp/book/1319)

## 1章「統計学とは～データ分析における統計学の役割～」
### 1.1 データ分析をする

データ分析の目的とは
①データを要約すること（記述統計量：平均、中央値、最頻値、分散、標準偏差）  
②対象を説明すること（相関関係、因果関係）  
③新しく得られるデータを予測すること  
である。

### 1.2    統計学の役割    
ばらつき（データに含まれる一つ一つの差異）は対象がもつ性質・関係性の本当の姿をぼかし、対象のを説明と予測を難しくする。
その`ばらつきに立ち向かう対処法`として統計学を使う。
統計学の根底にはばらつきや不確実性を確率として表現する確率論がある。

### 1.3    統計学の全体像
統計学の全体像は？  
    
* 記述統計  
* 推測統計 (統計的推定、 仮説検定）  

## 第2章 母集団と標本～データ分析の目的と対象を設定する～


### 2.1 データ分析の目的と興味の対象
    
データ分析を始めるにあたって、データ分析の目的と、興味の対象を明確に設定することが重要にになる。なぜなら、データ分析の目的によって、どのような実験・観測を通してデータを得るべきか、どのような分析をするべきかが変わってくるためである。


### 2.2 母集団
母集団とは興味の対象全体のまとまりのことである。    
また、有限母集団と無限母集団に分けることができ、母集団に含まれる要素の数を、母集団の大きさ、または母集団サイズという。有限母集団であれば、含まれるすべての要素を調べつくすことは原理的に可能であるが、無限母集団では、含まれる要素をすべて調べつくすことは原理的にできない。


### 2.3 母集団の性質を知る
母集団の持つ性質を求める方法はどのようなものがあるかを考える。
まず有限母集団について考える。有限母集団は全数調査して記述統計を用いることが可能である。しかし、コストを考慮すると全数調査は困難である。そこで、有限母集団でも無限母集団でも全数調査が必要ない方法として推測統計を用いる。
推測統計は母集団の一部を分析することで、母集団の全体を推測する枠組みである。

用語整理
* 標本（サンプル）：母集団の一部
* 標本抽出（サンプリング）：標本を母集団から取り出すこと
* 標本調査：標本から母集団の性質を調べること
* 標本の大きさ（サンプルサイズ、標本サイズ）：標本に含まれる要素の数
    ※標本の大きさは、推測の確からしさや、仮説検定の結果にもかかわるため重要な要素
* サンプル数：標本の数

## 第3章  統計分析の基礎～データの種類・統計量・確率～
### 3.1 データのタイプ
データ（変数）の種類には以下のようなものがある。
* 量的変数（連続変数、離散変数）
* 質的変数

### 3.2 データの分布
データの全体的な傾向を把握する方法として、ヒストグラムがよくつかわれる。
また、ヒストグラムの種類として以下の3つがある。
 * 離散型：横軸は数値、縦軸はその数値がデータに現れた個数（度数、カウント数）
* 連続型：横軸はビン幅、縦軸はビン幅に含まれる数値の個数
* カテゴリ変数：横軸は各カテゴリ、縦軸は各カテゴリのカウント数
連続型の場合、階級の決め方によって印象が変わるので、注意が必要。（スタージェスの公式を用いる）  
![CodeCogsEqn](https://user-images.githubusercontent.com/107327935/193429318-27a1e645-d0b2-486a-8ee4-f1241389f92b.svg)
 
[スタージェスの公式 | 統計用語集 | 統計WEB](https://bellcurve.jp/statistics/glossary/7445.html)

### 3.3 統計量
データを客観的かつ定量的にとらえる（要約する）方法として記述統計量がある。
代表的な記述統計量は以下のものがある。
* 代表値：平均値、中央値、最頻値
* ばらつきを表す値：分散、標準偏差

また、外れ値の影響を受ける統計量があるので、外れ値なのか、異常値なのかを判断する必要がある。異常値である場合は取り除く。（異常値：測定やデータ記録におけるミスによって記録された値）


### 3.4 確率
確率と統計のつながりを考える。
「母集団と標本データ」という扱いづらい対象が「確率分布とその実現値」という数学的に扱える対象に置き換えることができる。  

確率分布：横軸に確率変数を、縦軸に確率変数の起こりやすさを表した分布  

母集団から抽出された標本を、ある数学的な確率分布から生成された値だと仮定することによって分析を進めていくことが可能になる。
そして統計的推測とは、データからその生成元がどのような確率分布であるかを推測することにほかならない。


### 3.5 理論的な確率分布
 統計学で最も頻繁に登場する正規分布。  
![image](https://user-images.githubusercontent.com/107327935/193429325-cc66bf83-0713-4425-b7eb-0ed8965c447a.png)

μを平均、ρを標準偏差とすると、    
μ±ρまでの範囲が起こる確率が68％、μ±2ρで95％、μ±3ρで99.7%

## 第4章    推測統計～信頼区間（データから母集団の性質を推定する）
### 4.1 推測統計を学ぶ前に
この章は推測統計のポイント（直観的な理解）について説明されている。

基本的な考え方  
確率分布と実現値の関係は、母集団と標本の関係によく似ている。よって、「母集団＝確率分布」、「標本＝確率分布に従う実現値」として考えることができる。

推定における重要ポイント
* ポイント1
本当に興味があるのは、標本のデータではなく、母集団である。
* ポイント2
母集団のすべての要素を調べつくす全数調査は困難である。
* ポイント2
小さいサンプルサイズの標本から母集団を推測できる
* ポイント4
標本を抽出するときは、ランダムサンプリングする必要がある。


### 4.2 信頼区間
   
標本平均（手元にあるデータ）と母集団の平均（知りたい値）の誤差がどのような値になるかを知る方法として信頼区間を用いる。  

信頼区間  
信頼区間とは「〇〇％の確率で、この区間が母集団平均μを含んでいる」となる。※

標本誤差の確率分布について、正規分布に近似できると考えて平均値±2×標準偏差の範囲に約95％含まれるというのを利用して式変形する。（正確に言うと、平均±1.96×標準偏差の範囲が95%）よって、サンプルサイズnで得られた標本から計算した標本平均と標準偏差sから、母集団平均μの範囲を求めることができる。  
→これが信頼区間  

また、中心極限定理はサンプルサイズnが大きい時に近似的に成立するので、実際のデータ分析でみられるような小さいサンプルサイズの場合はt分布を利用する必要がある。  

精度を高めるには不偏標準偏差sを小さくするかサンプルサイズnを大きくする  

※母集団から標本をとってきて〇〇％信頼区間を求める、という作業を100回行ったときに平均的に〇〇回、その区間がμを含むということ。  

`用語集`  
* 標本誤差  
標本平均ー母集団平均（確率分布）  
確率分布は正規分布で近似でき、平均0、標準偏差ρ/√nになる。  

* 大数の法則  
標本平均と母集団の関係には、大数の法則が成り立つ。  
サンプルサイズnを大きくしていくと標本平均が母集団平均に限りなく近づくという法則。  
これを言い換えると、標本誤差が限りなく０に近づくということ。  

* 中心極限定理   
母集団がどのような分布であっても、サンプルサイズnが大きい時に標本平均の分布が正規分布で近似できることを意味する。  
平均：母集団平均μ  
標準偏差：ρ/√n  

* t分布  
母集団が正規分布であるという仮定の下、見てである母集団の標準偏差ρを、標本から計算した不偏標準偏差sで代用したときに、標準誤差をｓ/√nで割った値が従う分布。  

ｔ分布の特徴：正規分布とよく似た形状。サンプルサイズnに依存して形状が少し変化する（サンプルサイズnが大きくなるにつれてt分布は正規分布に近づく）  

* 推定量  
母集団の性質を推定するために使う統計量

* 一致推定量  
サンプルサイズnを無限大にしたときに推定量が母集団の性質に一致する推定量

* 不偏推定量  
推定量の平均値（期待値）が母集団の性質に一致する推定量

* 不偏標準偏差  
母集団の標準偏差の不偏推定量

