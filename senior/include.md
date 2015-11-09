Include
===

这两者的差别其他在正常的开发过程中并没那么纠结, 你用哪一个似乎都不会太大的影响, 当然如果你有代码洁癖, 你可以斟酌下具体使用情况.
有些人会拿效率说事, 如果为了这么点效率的话, 那就不应该用php语言, 毕竟PHP本省的执行效率就不快

用法
---

    incluce 在用到时加载
    require 在一开始就加载
    _once 后缀表示已加载的不加载


报错
---

    include引入文件的时候，如果碰到错误，会给出提示，并继续运行下边的代码。
    require引入文件的时候，如果碰到错误，会给出提示，并停止运行下边的代码。


条件引用
---

include() 与 require()的功能相同，用法上却有一些不同，include() 是有条件包含函数，而 require() 则是无条件包含函数。

* 如果变量$some为真，则将包含文件somefile.php

```php    
if($some) {  
　　include 'somefile.php';    
}
```

* 但无论$some取何值，下面的代码将把文件somefile.php包含进文件里

```php    
if($some) {    
　　require 'somefile.php';  
}
```
