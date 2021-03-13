synchronized 与lock区别

  synchronized是jvm底层实现
  lock是jdk层面的api实现
  
  synchronized通过wait（）/notify（）/notifyall（）来控制临界资源访问，
  lock是用过condition来同步临界资源，并且实现了公平锁，以及可以支持唤醒指定线程，并且可以绑定多个锁定条件，更加灵活
  
  synchronized只能等待线程执行完毕或者抛出异常来结束线程
  lock可以主动中断线程执行，可以设置超时方法
  
  synchronized不需要手动释放锁，不需要考虑死锁
  lock需要手动释放锁，并有可能会有死锁的情况发生
