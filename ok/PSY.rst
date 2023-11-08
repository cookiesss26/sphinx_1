.. vim: syntax=rst

PSY-MA 策略
=========

29.1计算方法
--------

PSY指的是在N天内的上涨天数占总天数的百分比。

.. math:: PSY\  = \frac{M(上涨天数)}{N(总天数)}*100

.. math:: PSYMA = SMA(PAY,N)

29.2策略逻辑
--------

做多：当PSY曲线向上突破PSYMA曲线；

做空：当PSY曲线向下跌破PSYMA曲线；
