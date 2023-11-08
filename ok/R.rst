.. vim: syntax=rst

R-Breaker策略
===========

R-Breaker策略基于市场的波动范围和支撑/阻力水平，计算出多个价格水平用于制定进出场点位。

30.1 计算方法
---------

.. math:: pivot = \frac{high + low + close}{3}

.. math:: 突破买入价：B_{Break}\_\  = \ high\  + \ 2\ *\ (pivot\  - \ low)

.. math:: 观察卖出价：S_{Setup}\  = \ pivot\  + \ (high\  - \ low)

.. math:: 反转卖出价：S_{Enter}\  = \ 2\ *\ pivot\ –\ low

.. math:: 反转买入价：B_{Enter}\  = \ 2\ *\ pivot\  - \ high

.. math:: 观察买入价：B_{Setup} = \ pivot\  - \ (high\  - \ low)

.. math:: 观察买入价：S_{Break}\  = \ low\  - \ 2\ *\ (high\  - \ pivot)

30.2策略逻辑
--------

（1）空仓：价格超过突破买入价，开多；价格跌破突破卖出价，开空。

（2）多头：持仓日内最高价超过观察卖出价后，盘中价格出现回落，且进一步跌破反转卖出价构成的支撑线，则反手做空。

（3）空头：持仓日内最低价低于观察买入价后，盘中价格出现反弹，且进一步超过反转买入价构成的阻力线，则反手做多。
