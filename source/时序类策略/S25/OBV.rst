.. vim: syntax=rst

OBV策略
=====

27.1 计算方法
---------

.. math::

   \left\{ \begin{array}{r} OBV\  = \ 前一个\ OBV\  + \ 当前交易量\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ {Close}_{t} > \ {Close}_{t - 1} \\ OBV\  = \ 前一个\ OBV - \
   当前交易量\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ {Close}_{t} < \ {Close}_{t - 1} \\ OBV\  = \ 前一个\ OBV\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \
   \ \ \ \ \ \ \ \ \ \ \ \ \ {Close}_{t} = \ {Close}_{t - 1} \end{array} \right.\

27.2策略逻辑
--------

做多：OBV向上突破OBV的移动平均线 (MA)；

做空：OBV向下跌破OBV的移动平均线 (MA)；
