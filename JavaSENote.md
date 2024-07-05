### 常用类和基础API

#### Java比较器

1.实现对象的排序，可以考虑两种方法：自然排序、定制排序

2. 方式一：实现Comparable接口的方式
    实现步骤：
  1. 具体的类A实现Comparable接口
  2. 重写compareTo方法



3. 方式二：实现comparator接口的方式

  实现步骤：

  1. 创建一个实现了comparator接口的实现类
  2. 实现类要求重写comparator接口中的抽象方法  

4. 对比两种方式：

   角度一：

   ​	自然排序：单一的、唯一的

   ​	定制排序：灵活的、多样的

   角度二：

   ​	自然排序：一劳永逸的

   ​	定制排序：临时的

   角度三：

   ​	自然排序：对应的接口是coomparable，对应的抽象方法是compareTo

   ​	定制排序：对应的接口是comparator，对应的抽象方法是compare

#### 其他常用类和基础API
1. System类
   - 属性：err、out、in
   - 方法：currentTimeMillis()、gc()、exit(int status)、getProperty(String property)
   
2. Runtime类

   > `public static Runtime getRuntime()`： 返回与当前 Java 应用程序相关的运行时对象。应用程序不能创建自己的 Runtime 类实例。
   >
   > `public long totalMemory()`：返回 Java 虚拟机中初始化时的内存总量。此方法返回的值可能随时间的推移而变化，这取决于主机环境。默认为物理电脑内存的1/64。
   >
   > `public long maxMemory()`：返回 Java 虚拟机中最大程度能使用的内存总量。默认为物理电脑内存的1/4。
   >
   > `public long freeMemory()`：回 Java 虚拟机中的空闲内存量。调用 gc 方法可能导致 freeMemory 返回值的增加。

3. Math类

4. BigInteger类和BigDecimal类

5. Random类

### 集合框架概述

1. 内存层面需要针对于多个数据进行存储。此时，可以考虑的容器有：数组、集合类
2. 数组存储多个数据方面的特点：
   - 数组一旦初始化，其长度就确定了。
   - 数组中的多个元素是依次紧密排列的，有序的，可重复的。
   - 数组中可用的方法和属性极少。具体的需要需要自己来组织相关的代码逻辑。
   - 数组一旦初始化完成，其元素的类型就是确定的，不是此类型的元素，就不能添加到此数组中。
   - 元素的类型既可以是基本数据类型，也可以是引用数据类型。
   - 针对于数组中元素的删除和插入操作性能较差


3. Java集合框架体系（java.util包下）
   - java.util.Collection
     - 子接口List：存储有序的、可重复的数据（“动态”数组）
       - ArrayList（主要实现类）
       - LinkedList
       - Vector
     - 子接口Set：存储无序的、不可重复的数据
       - HashSet
       - LinkedHashSet
       - TreeSet
   - java.util.Map：存储一对一对的数据（key-value键值对）  
     - HashMap
     - LinkedHashMap
     - TreeMap
     - Hashtable
     - Properties


4. 学习的程度把握：
   - 针对于具体的多个数据，知道选择相应的接口的主要实现类
   - 区分接口中不同实现类的区别
   - 针对于常用的实现类，熟悉底层的源码、熟悉常见的的数据结构
