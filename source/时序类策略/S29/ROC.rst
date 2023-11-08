.. vim: syntax=rst

ROC策略
=====

变动率指标ROC是拿当日的收盘价和n天前的收盘价做比较，n是参数。

30.1计算方法
--------

.. math:: ROC = \frac{{Close}_{t} - {Close}_{t - n}}{{Close}_{t - n}}

30.2策略逻辑
--------

做多：ROC向上突破0；

做空：ROC向下突破0。
