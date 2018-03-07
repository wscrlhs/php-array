
>收藏的PHP数组相关的知识

## table-of-contents 
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [索引数组](#%E7%B4%A2%E5%BC%95%E6%95%B0%E7%BB%84)
- [关联数组](#%E5%85%B3%E8%81%94%E6%95%B0%E7%BB%84)
- [多维数组](#%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84)
- [输出当前元素的值](#%E8%BE%93%E5%87%BA%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出最后一个元素的值](#%E8%BE%93%E5%87%BA%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出下一个元素的值](#%E8%BE%93%E5%87%BA%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出上一个元素的值](#%E8%BE%93%E5%87%BA%E4%B8%8A%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出第一个元素的值](#%E8%BE%93%E5%87%BA%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
- [输出当前元素的键名和键值，并将内部指针向前移动](#%E8%BE%93%E5%87%BA%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E9%94%AE%E5%90%8D%E5%92%8C%E9%94%AE%E5%80%BC%E5%B9%B6%E5%B0%86%E5%86%85%E9%83%A8%E6%8C%87%E9%92%88%E5%90%91%E5%89%8D%E7%A7%BB%E5%8A%A8)
- [统计元素数量](#%E7%BB%9F%E8%AE%A1%E5%85%83%E7%B4%A0%E6%95%B0%E9%87%8F)
- [输出当前元素键名](#%E8%BE%93%E5%87%BA%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E9%94%AE%E5%90%8D)
- [创建包含变量名和它们的值的数组](#%E5%88%9B%E5%BB%BA%E5%8C%85%E5%90%AB%E5%8F%98%E9%87%8F%E5%90%8D%E5%92%8C%E5%AE%83%E4%BB%AC%E7%9A%84%E5%80%BC%E7%9A%84%E6%95%B0%E7%BB%84)
- [从数组中将变量导入到当前的符号表](#%E4%BB%8E%E6%95%B0%E7%BB%84%E4%B8%AD%E5%B0%86%E5%8F%98%E9%87%8F%E5%AF%BC%E5%85%A5%E5%88%B0%E5%BD%93%E5%89%8D%E7%9A%84%E7%AC%A6%E5%8F%B7%E8%A1%A8)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->




## 索引数组   
带有数字索引的数组

```php
$cars=array("Volvo","BMW","SAAB");

//or
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="SAAB";
```
<br>[⬆ Back to top](##table-of-contents)

## 关联数组
使用您分配给数组的指定键的数组。

```php
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

//or
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```
<br>[⬆ Back to top](##table-of-contents)

## 多维数组
包含一个或多个数组的数组。

```php
$cars = array
  (
  array("Volvo",22,18),
  array("BMW",15,13),
  );

//or
$cars[0][0] = 'Volvo' ;
$cars[0][1] = 22;
$cars[0][2] = 18 ;
$cars[1][0] = 'BMW';
$cars[1][0] = 15;
$cars[1][0] = 13;
```
<br>[⬆ Back to top](##table-of-contents)

## 输出当前元素的值
**current()**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo current($people) ; // 当前元素是 Bill
```
<br>[⬆ Back to top](##table-of-contents)

## 输出最后一个元素的值
**end()**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo end($people) ; // 最后一个元素是 David
```
<br>[⬆ Back to top](##table-of-contents)

## 输出下一个元素的值
**next()**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo next($people) ; // Bill 的下一个元素是 Steve
```
<br>[⬆ Back to top](##table-of-contents)

## 输出上一个元素的值
**prev()**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo prev($people) ; // David 之前的元素是 Mark
```
<br>[⬆ Back to top](##table-of-contents)


## 输出第一个元素的值
**reset()**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo reset($people) ; // 把内部指针移动到数组的首个元素，即 Bill
```
<br>[⬆ Back to top](##table-of-contents)

## 输出当前元素的键名和键值，并将内部指针向前移动
**each()**
```php
$people = array("Bill", "Steve", "Mark", "David");

each($people) ; // 返回当前元素的键名和键值，即'0'=> Bill
echo current($people); //并将内部指针向前移动, 即Steve
```
<br>[⬆ Back to top](##table-of-contents)

##  统计元素数量
**count()**
```php
$a = array(0,1,2,3);

echo count($a); // 4
```
<br>[⬆ Back to top](##table-of-contents)

## 输出当前元素键名
**key()**
```php
$a = array('key'=>'value');

echo key($a); // key
```
<br>[⬆ Back to top](##table-of-contents)

## 创建包含变量名和它们的值的数组
**compact()**
```php
$firstname = "Bill";
$lastname = "Gates";
$age = "60";

$result = compact("firstname", "lastname", "age");

print_r($result); // Array ( [firstname] => Bill [lastname] => Gates [age] => 60 )
```
<br>[⬆ Back to top](##table-of-contents)

## 从数组中将变量导入到当前的符号表
**extract()**
```php
$var_array = array("color" => "blue",
                   "size"  => "medium",
                   "shape" => "sphere");
extract($var_array);

echo "$color, $size, $shape"; // blue, medium, sphere
```
<br>[⬆ Back to top](##table-of-contents)
