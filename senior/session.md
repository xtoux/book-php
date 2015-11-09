Session
===

Session 定义
---

当您运行一个应用程序时，您会打开它，做些更改，然后关闭它。这很像一次会话。计算机清楚你是谁。它知道你何时启动应用程序，并在何时终止。但是在因特网上，存在一个问题：服务器不知道你是谁以及你做什么，这是由于 HTTP 地址不能维持状态。


开始 Session
---

在您把用户信息存储到 session 中之前，首先必须启动会话
注释：session_start() 函数必须位于 <html> 标签之前：

```php
<?php session_start(); ?>
<html>
<body>

</body>
</html>
```

保存和获取 Session

```php
<?php
session_start();
// store session data
$_SESSION['views']=1;
?>
<html>
<body>

<?php
//retrieve session data
echo "Pageviews=". $_SESSION['views'];
?>
</body>
</html>
```

终结 Session
---

如果您希望删除某些 session 数据，可以使用 unset() 或 session_destroy() 函数

* unset() 函数用于释放指定的 session 变量

```php
<?php
unset($_SESSION['views']);
?>
```

* session_destroy() 函数彻底终结 session

```php
<?php
session_destroy();
?>
```
