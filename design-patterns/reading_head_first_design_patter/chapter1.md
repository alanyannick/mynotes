# chapter 1



* 当涉及到维护时，为了复用（reuse）而使用继承的结局并不完美！ **因为可能某些子类并不具有超类的一些方法** ， 比如，鸭子的 `飞` 方法， 橡皮鸭可不会飞。
* 如果有一种建立软件的方法，好让我们对 **既有的代码影响最小的方式来修改** 软件该有多好。



**关于鸭子**

模拟鸭子游戏：需要各种各样的鸭子，鸭子可能会有的行为有：

* 飞 （不一定所有的鸭子都能飞，不一定所有的鸭子飞的方式都一样）
* 叫 （不一定所有的鸭子都能叫，不一定所有的鸭子叫的方式都一样）

基于下面给出的设计原则：**找出应用中可能需要的变化之处，将他们独立出来。** 所以我们就需要将 `飞` 和 `叫` 独立出来。建立一组新类来代表每个行为。



## 设计原则

* 找出应用中**可能需要变化之处**，把他们独立出来，不要让它们和那些不需要变换的代码混在一起
  * 如何找到可能需要变化之处呢？ 每次当新新需求到来的时，需要修改的地方
  * 把需要变化的部分**取出来并封装**起来， 以便可以轻松的改动或扩充此部分，而不影响其它不需要变化的部分
* 针对**接口**编程， 而不是针对实现编程。（因为所有的子类对象对可以用接口 来接收，这样在接收时就能同意口径），这里感觉应该嫁个条件（对于**变化之处** 针对接口编程）。
  * 这句话隐藏意思是： 实例对象 尽量赋值给 接口对象。



**所有的设计模式都提供了一套方法：系统中的某部分改变不会影响其它部分！**
