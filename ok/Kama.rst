.. vim: syntax=rst

Kama 策略
=======

用考夫曼自适应性移动平均线（KAMA）来代替短期均线，用短期均线与长期均线的相对位置关系，和相对强弱指标形成买卖依据。

21.1计算方法
--------

.. math:: kama_{t} = {close}_{t}*a_{t} + (1 - a_{t})kama_{t - 1}

.. math:: a_{t} = \left( e_{t}(f - s) + s \right)^{2}

.. math:: e_{t} = \frac{\left| in_{t} - in_{t - n} \right|}{\sum_{i = 0}^{n - 1}\mspace{2mu}\left| in_{t - i} - in_{t - i - 1} \right|}

.. math:: f = \frac{2}{2 + 1}

.. math:: s = \frac{2}{30 + 1}

其中，效率系数\ :math:`e_{t}`\ 代表价格变化的效率，\ :math:`f`\ 为最快的平滑系数，\ :math:`s`\ 为最慢的平滑系数

21.2策略逻辑
--------

（1）空仓： KAMA与MA的指标值的差值序列上穿零值序列，并且K线收盘价大于KAMA最新指标值，开多； KAMA与MA的指标值的差值序列下穿零值序列，并且K线收盘价小于KAMA最新指标值，开空。

（2）多头：KAMA与MA的指标值的差值序列下穿零值序列，平多。

（3）空头：KAMA与MA的指标值的差值序列上穿零值序列，平空。
