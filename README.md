# TouchUNIT

<img src="https://github.com/akita11/TouchUNIT/blob/main/TouchUNIT.jpg" width="320px">

タッチセンサICの[TTP223N-HA6](https://www.lcsc.com/product-detail/Touch-Sensors_Tontek-Design-Tech-TTP223N-HA6_C93723.html)を使用した、2系統のタッチセンサです。Grove端子の2本の信号線にタッチ状態を出力することができます。M5Stackの2個の物理スイッチがある[デュアルボタンUNIT](https://www.switch-science.com/products/4048)と同等の出力のため、UIFlow等ではこのデュアルボタンUNIT用のブロック・プログラムがそのまま使えます。

※[M5Stack用ADCユニット](https://www.switch-science.com/products/9491)と形状が互換なので、そのケースを流用できます。

## 使い方

オレンジのネジ端子にタッチ電極を接続します。T1とT2の独立の2系統のタッチ検出を使用できます。手を近づけただけでONとなるなどタッチ検出の感度が高すぎる場合は、後述の方法で感度を調整してください。（標準状態より感度を高めることは原理上できません）


## 設定の変更

### タッチ検出の感度の変更

基板上にコンデンサを取り付けることで、タッチ検出の感度を調整（低くする）ことができます。実際の使用状況にあわせて、適切な容量のコンデンサを接続してください。容量値や動作原理などはタッチ検出IC(TTP223N)のデータシートを参照してください。

- T1 : C3（1608サイズ表面実装）またはC4（挿入実装）
- T2 : C5（1608サイズ表面実装）またはC6（挿入実装）


### 出力信号の極性・トグルの設定

<img src="https://github.com/akita11/TouchUNIT/blob/main/TouchUNIT_back.jpg" width="320px">

基板裏面の半田ジャンパによって、出力の動作モードを設定できます。詳細はタッチ検出IC(TTP223N)のデータシートと回路図を参照してください。

- POL1(JP1/T1用)/POL2(JP3/T2用): ショート（標準設定）=タッチ時'0'／開放（パターンカット）=タッチ時'1'
- TOG1(JP2/T1用)/TOG2(JP4/T2用): 開放（標準設定）=タッチ時のみ0/1／ショート（半田を盛る）=タッチごとに出力がトグル

## Author

Junichi Akita (akita@ifdl.jp, @akita11)





