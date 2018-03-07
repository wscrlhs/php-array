
>收藏的PHP数组相关的知识，随插随用。

# table-of-contents 
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [索引数组](#%E7%B4%A2%E5%BC%95%E6%95%B0%E7%BB%84)
- [关联数组](#%E5%85%B3%E8%81%94%E6%95%B0%E7%BB%84)
- [多维数组](#%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84)
- [输出数组中当前元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出数组中的最后一个元素](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0)
- [输出数组中下一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出数组中上一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8A%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [数组内部指针重置到第一个元素](#%E6%95%B0%E7%BB%84%E5%86%85%E9%83%A8%E6%8C%87%E9%92%88%E9%87%8D%E7%BD%AE%E5%88%B0%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0)
- [返回当前元素的键名和键值，并将内部指针向前移动](#%E8%BF%94%E5%9B%9E%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E9%94%AE%E5%90%8D%E5%92%8C%E9%94%AE%E5%80%BC%E5%B9%B6%E5%B0%86%E5%86%85%E9%83%A8%E6%8C%87%E9%92%88%E5%90%91%E5%89%8D%E7%A7%BB%E5%8A%A8)
- [统计数组元素数量](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E5%85%83%E7%B4%A0%E6%95%B0%E9%87%8F)

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
<br>[⬆ Back to top](#table-of-contents)

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
<br>[⬆ Back to top](#table-of-contents)

## 多维数组
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
<br>[⬆ Back to top](#table-of-contents)

## 输出数组中当前元素的值
current()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo current($people) ; // 当前元素是 Bill
```
<br>[⬆ Back to top](#table-of-contents)

## 输出数组中的最后一个元素
end()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo end($people) ; // 最后一个元素是 David
```
<br>[⬆ Back to top](#table-of-contents)

## 输出数组中下一个元素的值
next()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo next($people) ; // Bill 的下一个元素是 Steve
```
<br>[⬆ Back to top](#table-of-contents)

## 输出数组中上一个元素的值
prev()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo prev($people) ; // David 之前的元素是 Mark
```
<br>[⬆ Back to top](#table-of-contents)


## 数组内部指针重置到第一个元素
reset()
```php
$people = array("Bill", "Steve", "Mark", "David");

echo reset($people) ; // 把内部指针移动到数组的首个元素，即 Bill
```
<br>[⬆ Back to top](#table-of-contents)

## 返回当前元素的键名和键值，并将内部指针向前移动
each()
```php
$people = array("Bill", "Steve", "Mark", "David");

each($people) ; // 返回当前元素的键名和键值，即 Bill
echo current($people); //并将内部指针向前移动, 即Steve
```
<br>[⬆ Back to top](#table-of-contents)

##  统计数组元素数量
count()
```php
$a = array(0,1,2,3);
var_dump(count($a));
//output
int 4
```
<br>[⬆ Back to top](#table-of-contents)

