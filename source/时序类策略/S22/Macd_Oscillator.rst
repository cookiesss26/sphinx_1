.. vim: syntax=rst

Macd Oscillator策略
=================

23.1 计算方法
---------

MACD反应移动平均线彼此靠近（收敛）或远离彼此（背离）的运动。

.. math:: (12\ day\ EMA\ –\ 26\ day\ EMA)\  = \ MACD

.. math:: {EMA}_{t}(N) = \text{ }{close}_{t}\text{ } \times \frac{\text{ }\text{平滑因子}\text{ }}{N + 1} + \text{ }{EMA}_{t - 1}\text{ } \times (1 - \frac{\text{ }\text{平滑因子}\text{ }}{N + 1})

:math:`\text{平滑因子}`\ 一般设定为2

注：这里的MACD和广义的MACD计算方式不同。

23.2策略逻辑
--------

做多：短期EMA上穿长期EMA

做空：短期EMA下穿长期EMA
