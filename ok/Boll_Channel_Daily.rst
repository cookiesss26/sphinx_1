.. vim: syntax=rst

Boll Channel Daily策略
====================

VNPY的原生布林通道策略，其实并非单因子策略，使用了boll、cci和atr指标。

9.1 计算方法
--------

多头止损线：

.. math:: long\_ stop\  = \ intra\_ trade\_ high（近期最高价） - \ atr\_ value\ *\ sl\_ multiplier

空头止损线：

.. math:: short\_ stop\  = \ intra\_ trade\_ low（近期最低价）\  + \ atr\_ value\ *\ sl\_ multiplier

9.2策略逻辑
-------

（1）空仓：如果价格大于布林上轨，且cci大于0，则开多；如果价格小于布林下轨，且cci小于0，则开空。

（2）多头：价格跌破多头止损线则平多。

（3）空头：价格突破空头止损线则平空。
