#Random类
Random()
以当前时间为种子创建一个Random对象

Random(seed:long)
以一个指定种子创建一个Random对象

nextInt():int
返回一个随机int值

nextInt(n:int):int
返回一个0到n(不包含n)之间的随机int值

---
创建一个Random对象时，必须指定一个种子或者使用默认的种子 如果两个对象有相同的种子，那他们键产生相同的的数的序列
