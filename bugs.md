# Bug

## 梯度下降法部分

目前測試都正確，solveXy, solveMatXy, solveLearnXy, optimizeAddTest.js, optimizeSumTest.js 等都可以正常運作並找到解答！


## 神經網路部分

單層神經網路像 perceptron.js, neuron.js 都可以正確運作。

多層 mlp 程式，像是 mlpXor, mlp7seg 學習都無法正確學習，看來像是梯度消失 (sigmoid) 與爆炸 (tanh) 的問題，但我不知道該如何解決。

```
$ node mlpXor.js
...
998:
  0 => x1:-0.000521 x2:-0.000430 f:0.484169
  1 => x1:0.000529 x2:1.000433 f:0.499247
  2 => x1:1.000523 x2:0.000459 f:0.506978
  3 => x1:0.999444 x2:0.999550 f:0.508833
  ==> energy = 1.0127289961823827
999:
  0 => x1:-0.000520 x2:-0.000430 f:0.484179
  1 => x1:0.000528 x2:1.000433 f:0.499252
  2 => x1:1.000523 x2:0.000459 f:0.506973
  3 => x1:0.999445 x2:0.999550 f:0.508823
  ==> energy = 1.0127279802856755
```