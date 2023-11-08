.. vim: syntax=rst

MACD Signal策略
=============

MACD 指标策略：由快、慢均线的离散、聚合来显示当前的多空状态和价格的发展变化趋势。

24.1 计算方法
---------

.. math:: {EMA}_{t}(N) = \text{ }{close}_{t}\text{ } \times \frac{\text{ }\text{平滑因子}\text{ }}{N + 1} + \text{ }{EMA}_{t - 1}\text{ } \times 1 - \frac{\text{ }\text{平滑因子}\text{ }}{N + 1}

（\ :math:`\text{平滑因子}`\ 一般设定为2）

.. math:: DIF = EMA(12) - EMA(26)

.. math:: MACD = EMA(DIF,9)

.. math:: DEA = \frac{{DIF}_{t} \times 2 + {DIF}_{t - 1} \times 8}{10}

24.1 策略逻辑
---------

做多：DIF上穿DEA

做空：DIF下穿DEA
