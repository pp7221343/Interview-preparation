# cas
* CAS是指Compare And Swap，比较并交换，是一种很重要的同步思想。如果主内存的值跟期望值一样，那么就进行修改，否则一直重试，直到一致为止。
* 底层通过**volatile**和**unsafe类**实现，unsafe是native，底层调用内存

## 缺点
* CAS实际上是一种自旋锁
* 一直循环，开销比较大。
* 只能保证一个变量的原子操作，多个变量依然要加锁。
* **引出了ABA问题**

### ABA问题
* 通过版本号解决
* 相关类：AtomicStampedReference（关注版本号，即reference的值被修改了多少次） 以及 AtomicMarkableReference（用boolean mark来标记reference是否被修改过）
