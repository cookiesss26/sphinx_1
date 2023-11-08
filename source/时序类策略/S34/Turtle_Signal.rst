.. vim: syntax=rst

Turtle Signal策略
===============

14.1计算方法
--------

唐安奇通道：

.. math:: 上轨\  = \ Max\left. （最高价，n \right.），\ n日最高价的最大值

.. math:: 下轨\  = \ Min\left. （最低价，n \right.），n日最低价的最小值

.. math:: 中轨\  = \ \frac{(上轨 + 下轨)}{2}

14.2策略逻辑
--------

做多：价格冲破上轨

做空：价格跌破下轨

多头：止损价格 = :math:`上轨 - 2 \times ATR`

空头：止损价格 = :math:`下轨 + 2 \times ATR`

仓位控制：根据持仓数量判断买入与卖出价格
