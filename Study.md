# 未知入力オブザーバ
> 未知入力オブザーバを用いたペダリングトルク推定  
> https://library.naist.jp/mylimedio/dllimedio/showpdf2.cgi/DLPDFR009769_P1-42

---
## オブザーバの種類？
- Luenberger
- 予測型
- UIO 未知入力オブザーバ


memo:Ctrl+Alt+Vでクリップボード貼り付け。

---
## 一般構造化オブザーバの定義：  
![](2017-12-05-19-54-30.png)

これで推定値と真値の誤差が0に漸近する場合が一般構造化オブザーバである。

G1が0であればこれはLuenbergの全次元オブザーバである。

--

UIOにおける状態方程式を次に示す。  
![](2017-12-05-20-01-35.png)

uが観測可能な入力でdは観測不可能な入力である。

---
## Cheokの一般構造化OBSを適用すると？

![](2017-12-05-20-04-43.png)

![](2017-12-05-20-07-29.png)

--

![](2017-12-05-20-08-53.png)

出力で観測できる変数の数が未知入力数をこえていれば安定だけどそうでない場合は別のオブザーバを組む必要があるそうな。

補助出力方程式というらしいぞ。

---
## Platooning Controlについて
Plattoning 制御について調べる。


### Lecture
http://www.mogi.bme.hu/TAMOP/jarmurendszerek_iranyitasa_angol/math-ch11.html

![](2017-12-11-23-25-10.png)

ここで，距離が0になる時に加速度を0にするように制御するのが定石らしい。

### Paper1 ：センサのゆらぎとフィルタ特性の影響
https://www.jstage.jst.go.jp/article/ieejias1987/114/11/114_11_1149/_pdf

重要ワード：「距離のセンサにはノイズ除去のセンサを使うが」ナイスワード。
この観測のフィルタと制御のフィルタを比較することが 目的になります。

加速度指令値で制御する。確かに？
この辺はうまく考える必要がありそう。



### Paper2：

