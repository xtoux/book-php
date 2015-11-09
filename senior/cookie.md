Cookie
===

Cookie是用户将数据保存在客户端浏览器的地方, 最直观的用法是购物车. 如果你在jd或tm买东西, 没登录的时候, 你依然可以将商品添加到购物车,
而这个时候数据就保存在cookie中 

Cookie定义
---

cookie 常用于识别用户, cookie 是服务器留在用户计算机中的小文件, 每当相同的计算机通过浏览器请求页面时，它同时会发送 cookie


创建 cookie
---

    setcookie() 函数用于设置 cookie。
    setcookie(name, value, expire, path, domain);

    注释：setcookie() 函数必须位于 <html> 标签之前。

```php
<?php
setcookie("user", "Alex Porter", time()+3600);
?>
<html>
<body>

</body>
</html>
```

读取 Cookie
---

PHP 的 $_COOKIE 变量用于取回 cookie 的值

```php
<?php
// Print a cookie
echo $_COOKIE["user"];

// A way to view all cookies
print_r($_COOKIE);
?>
```

使用 isset() 函数来确认是否已设置了 cookie

```php
<html>
<body>
<?php
if (isset($_COOKIE["user"])) {
  echo "Welcome " . $_COOKIE["user"] . "!<br />";
} else {
  echo "Welcome guest!<br />";
}
?>
</body>
</html>
```

何删除 cookie
---

当删除 cookie 时，您应当使过期日期变更为过去的时间点。

```php
<?php
// set the expiration date to one hour ago
setcookie("user", "", time()-3600);
?>
```
