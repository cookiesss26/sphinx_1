.. vim: syntax=rst

MACD策略
======

25.1 计算方法
---------

.. math:: DIF = EMA(12) - EMA(26)

.. math:: MACD = EMA(DIF,9)

25.2策略逻辑
--------

做多：DIF、DEA 均为正且 MACD 由负转正；

做空：DIF、DEA 均为负且 MACD 由正转负；
