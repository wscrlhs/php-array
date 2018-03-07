
>收藏的PHP数组相关的知识，随插随用。
# table-of-contents 
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [索引数组](#%E7%B4%A2%E5%BC%95%E6%95%B0%E7%BB%84)
- [关联数组](#%E5%85%B3%E8%81%94%E6%95%B0%E7%BB%84)
- [多位数组](#%E5%A4%9A%E4%BD%8D%E6%95%B0%E7%BB%84)
- [统计数组元素数量](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E5%85%83%E7%B4%A0%E6%95%B0%E9%87%8F)
- [数组中当前元素的值](#%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->




## 索引数组   
带有数字索引的数组

```php
//第一种方式
$cars=array("Volvo","BMW","SAAB");

//第二种方式
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="SAAB";
```
<br>[⬆ Back to top](table-of-contents)

## 关联数组
关联数组是使用您分配给数组的指定键的数组。

```php
//第一种方式
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

//第二种方式
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```
<br>[⬆ Back to top](table-of-contents)

## 多位数组
多维数组指的是包含一个或多个数组的数组。

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
<br>[⬆ Back to top](table-of-contents)

##  统计数组元素数量
count()
```php
$a = array(0,1,2,3);
var_dump(count($a));
//output
int 4
```
<br>[⬆ Back to top](table-of-contents)

## 数组中当前元素的值
current()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo current($people) . "<br>"; // 当前元素是 Bill
echo next($people) . "<br>"; // Bill 的下一个元素是 Steve
echo current($people) . "<br>"; // 现在当前元素是 Steve
echo prev($people) . "<br>"; // Steve 的上一个元素是 Bill
echo end($people) . "<br>"; // 最后一个元素是 David
echo prev($people) . "<br>"; // David 之前的元素是 Mark
echo current($people) . "<br>"; // 目前的当前元素是 Mark
echo reset($people) . "<br>"; // 把内部指针移动到数组的首个元素，即 Bill
echo next($people) . "<br>"; // Bill 的下一个元素是 Steve

print_r (each($people)); // 返回当前元素的键名和键值（目前是 Steve），并向前移动内部指针
```
<br>[⬆ Back to top](table-of-contents)


