<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of Contents  

- [类型](#%E7%B1%BB%E5%9E%8B)
- [数组函数](#%E6%95%B0%E7%BB%84%E5%87%BD%E6%95%B0)
- [自定义函数](#%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

>收藏的PHP数组相关的知识，随插随用。

##  类型 
>数组是特殊的变量，它可以同时保存一个以上的值。

- 索引数组   
带有数字索引的数组

<details>
<summary>Examples</summary>

```php
//第一种方式
$cars=array("Volvo","BMW","SAAB");

//第二种方式
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="SAAB";
```

</details>

<br>[⬆ Back to top](#table-of-contents)


- 关联数组
关联数组是使用您分配给数组的指定键的数组。

<details>
<summary>Examples</summary>

```php
//第一种方式
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

//第二种方式
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```

</details>

<br>[⬆ Back to top](#table-of-contents)


- 多位数组
多维数组指的是包含一个或多个数组的数组。
<details>
<summary>Examples</summary>

```php
//第一种方式
$cars = array
  (
  array("Volvo",22,18),
  array("BMW",15,13),
  );

//第二种方式
$cars[0][0] = 'Volvo' ;
$cars[0][1] = 22;
$cars[0][2] = 18 ;
$cars[1][0] = 'BMW';
$cars[1][0] = 15;
$cars[1][0] = 13;
```

</details>

<br>[⬆ Back to top](#table-of-contents)





## 数组函数


## 自定义函数


