## 收藏的PHP数组相关的知识
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## table-of-contents 

- [类型](#%E7%B1%BB%E5%9E%8B)
  - [索引数组](#%E7%B4%A2%E5%BC%95%E6%95%B0%E7%BB%84)
  - [关联数组](#%E5%85%B3%E8%81%94%E6%95%B0%E7%BB%84)
  - [多维数组](#%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84)
- [获取](#%E8%8E%B7%E5%8F%96)
  - [输出数组中当前元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中最后一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中下一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中上一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8A%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中第一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中当前元素的键名和键值，并将内部指针向前移动](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E9%94%AE%E5%90%8D%E5%92%8C%E9%94%AE%E5%80%BC%E5%B9%B6%E5%B0%86%E5%86%85%E9%83%A8%E6%8C%87%E9%92%88%E5%90%91%E5%89%8D%E7%A7%BB%E5%8A%A8)
  - [输出数组中当前元素键名](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E9%94%AE%E5%90%8D)
  - [返回数组中部分的或所有的键名](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E9%83%A8%E5%88%86%E7%9A%84%E6%88%96%E6%89%80%E6%9C%89%E7%9A%84%E9%94%AE%E5%90%8D)
  - [返回数组中所有的值](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E7%9A%84%E5%80%BC)
  - [返回数组中指定的一列](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E6%8C%87%E5%AE%9A%E7%9A%84%E4%B8%80%E5%88%97)
- [操作](#%E6%93%8D%E4%BD%9C)
  - [将数组中的所有键名修改为全大写或小写](#%E5%B0%86%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%89%80%E6%9C%89%E9%94%AE%E5%90%8D%E4%BF%AE%E6%94%B9%E4%B8%BA%E5%85%A8%E5%A4%A7%E5%86%99%E6%88%96%E5%B0%8F%E5%86%99)
  - [从数组中取出一段](#%E4%BB%8E%E6%95%B0%E7%BB%84%E4%B8%AD%E5%8F%96%E5%87%BA%E4%B8%80%E6%AE%B5)
  - [把数组中的值赋给一组变量](#%E6%8A%8A%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E5%80%BC%E8%B5%8B%E7%BB%99%E4%B8%80%E7%BB%84%E5%8F%98%E9%87%8F)
  - [建立一个包含指定范围单元的数组](#%E5%BB%BA%E7%AB%8B%E4%B8%80%E4%B8%AA%E5%8C%85%E5%90%AB%E6%8C%87%E5%AE%9A%E8%8C%83%E5%9B%B4%E5%8D%95%E5%85%83%E7%9A%84%E6%95%B0%E7%BB%84)
  - [打乱数组](#%E6%89%93%E4%B9%B1%E6%95%B0%E7%BB%84)
  - [移除数组中重复的值](#%E7%A7%BB%E9%99%A4%E6%95%B0%E7%BB%84%E4%B8%AD%E9%87%8D%E5%A4%8D%E7%9A%84%E5%80%BC)
  - [创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值](#%E5%88%9B%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%94%A8%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%80%BC%E4%BD%9C%E4%B8%BA%E5%85%B6%E9%94%AE%E5%90%8D%E5%8F%A6%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%80%BC%E4%BD%9C%E4%B8%BA%E5%85%B6%E5%80%BC)
  - [创建包含变量名和它们的值的数组](#%E5%88%9B%E5%BB%BA%E5%8C%85%E5%90%AB%E5%8F%98%E9%87%8F%E5%90%8D%E5%92%8C%E5%AE%83%E4%BB%AC%E7%9A%84%E5%80%BC%E7%9A%84%E6%95%B0%E7%BB%84)
  - [从数组中将变量导入到当前的符号表](#%E4%BB%8E%E6%95%B0%E7%BB%84%E4%B8%AD%E5%B0%86%E5%8F%98%E9%87%8F%E5%AF%BC%E5%85%A5%E5%88%B0%E5%BD%93%E5%89%8D%E7%9A%84%E7%AC%A6%E5%8F%B7%E8%A1%A8)
- [排序](#%E6%8E%92%E5%BA%8F)
  - [对数组排序,由低到高](#%E5%AF%B9%E6%95%B0%E7%BB%84%E6%8E%92%E5%BA%8F%E7%94%B1%E4%BD%8E%E5%88%B0%E9%AB%98)
  - [对数组逆向排序,由高到低](#%E5%AF%B9%E6%95%B0%E7%BB%84%E9%80%86%E5%90%91%E6%8E%92%E5%BA%8F%E7%94%B1%E9%AB%98%E5%88%B0%E4%BD%8E)
  - [对数组按照键名排序,由低到高](#%E5%AF%B9%E6%95%B0%E7%BB%84%E6%8C%89%E7%85%A7%E9%94%AE%E5%90%8D%E6%8E%92%E5%BA%8F%E7%94%B1%E4%BD%8E%E5%88%B0%E9%AB%98)
  - [对数组按照键名逆向排序,由高到低](#%E5%AF%B9%E6%95%B0%E7%BB%84%E6%8C%89%E7%85%A7%E9%94%AE%E5%90%8D%E9%80%86%E5%90%91%E6%8E%92%E5%BA%8F%E7%94%B1%E9%AB%98%E5%88%B0%E4%BD%8E)
  - [对数组进行排序并保持索引关系,由低到高](#%E5%AF%B9%E6%95%B0%E7%BB%84%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%E5%B9%B6%E4%BF%9D%E6%8C%81%E7%B4%A2%E5%BC%95%E5%85%B3%E7%B3%BB%E7%94%B1%E4%BD%8E%E5%88%B0%E9%AB%98)
  - [对数组进行逆向排序并保持索引关系,由高到低](#%E5%AF%B9%E6%95%B0%E7%BB%84%E8%BF%9B%E8%A1%8C%E9%80%86%E5%90%91%E6%8E%92%E5%BA%8F%E5%B9%B6%E4%BF%9D%E6%8C%81%E7%B4%A2%E5%BC%95%E5%85%B3%E7%B3%BB%E7%94%B1%E9%AB%98%E5%88%B0%E4%BD%8E)
  - [使用用户自定义的比较函数对数组中的值进行排序](#%E4%BD%BF%E7%94%A8%E7%94%A8%E6%88%B7%E8%87%AA%E5%AE%9A%E4%B9%89%E7%9A%84%E6%AF%94%E8%BE%83%E5%87%BD%E6%95%B0%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E5%80%BC%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F)
  - [使用用户自定义的比较函数对数组中的值进行排序并保持索引关联](#%E4%BD%BF%E7%94%A8%E7%94%A8%E6%88%B7%E8%87%AA%E5%AE%9A%E4%B9%89%E7%9A%84%E6%AF%94%E8%BE%83%E5%87%BD%E6%95%B0%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E5%80%BC%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%E5%B9%B6%E4%BF%9D%E6%8C%81%E7%B4%A2%E5%BC%95%E5%85%B3%E8%81%94)
  - [使用用户自定义的比较函数对数组中的键名进行排序](#%E4%BD%BF%E7%94%A8%E7%94%A8%E6%88%B7%E8%87%AA%E5%AE%9A%E4%B9%89%E7%9A%84%E6%AF%94%E8%BE%83%E5%87%BD%E6%95%B0%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E9%94%AE%E5%90%8D%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F)
  - [用“自然排序”算法对数组排序](#%E7%94%A8%E8%87%AA%E7%84%B6%E6%8E%92%E5%BA%8F%E7%AE%97%E6%B3%95%E5%AF%B9%E6%95%B0%E7%BB%84%E6%8E%92%E5%BA%8F)
  - [用“自然排序”算法对数组进行不区分大小写字母的排序](#%E7%94%A8%E8%87%AA%E7%84%B6%E6%8E%92%E5%BA%8F%E7%AE%97%E6%B3%95%E5%AF%B9%E6%95%B0%E7%BB%84%E8%BF%9B%E8%A1%8C%E4%B8%8D%E5%8C%BA%E5%88%86%E5%A4%A7%E5%B0%8F%E5%86%99%E5%AD%97%E6%AF%8D%E7%9A%84%E6%8E%92%E5%BA%8F)
- [统计检查](#%E7%BB%9F%E8%AE%A1%E6%A3%80%E6%9F%A5)
  - [统计数组中元素数量](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E4%B8%AD%E5%85%83%E7%B4%A0%E6%95%B0%E9%87%8F)
  - [统计数组中所有的值](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E7%9A%84%E5%80%BC)
  - [检查数组里是否有指定的键名或索引](#%E6%A3%80%E6%9F%A5%E6%95%B0%E7%BB%84%E9%87%8C%E6%98%AF%E5%90%A6%E6%9C%89%E6%8C%87%E5%AE%9A%E7%9A%84%E9%94%AE%E5%90%8D%E6%88%96%E7%B4%A2%E5%BC%95)
  - [检查数组中是否存在某个值](#%E6%A3%80%E6%9F%A5%E6%95%B0%E7%BB%84%E4%B8%AD%E6%98%AF%E5%90%A6%E5%AD%98%E5%9C%A8%E6%9F%90%E4%B8%AA%E5%80%BC)
- [分割合并替换](#%E5%88%86%E5%89%B2%E5%90%88%E5%B9%B6%E6%9B%BF%E6%8D%A2)
  - [将一个数组分割成多个](#%E5%B0%86%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E5%88%86%E5%89%B2%E6%88%90%E5%A4%9A%E4%B8%AA)
  - [合并一个或多个数组](#%E5%90%88%E5%B9%B6%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E6%95%B0%E7%BB%84)
  - [递归地合并一个或多个数组](#%E9%80%92%E5%BD%92%E5%9C%B0%E5%90%88%E5%B9%B6%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E6%95%B0%E7%BB%84)
  - [使用传递的数组替换第一个数组的元素](#%E4%BD%BF%E7%94%A8%E4%BC%A0%E9%80%92%E7%9A%84%E6%95%B0%E7%BB%84%E6%9B%BF%E6%8D%A2%E7%AC%AC%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%85%83%E7%B4%A0)
  - [使用传递的数组递归替换第一个数组的元素](#%E4%BD%BF%E7%94%A8%E4%BC%A0%E9%80%92%E7%9A%84%E6%95%B0%E7%BB%84%E9%80%92%E5%BD%92%E6%9B%BF%E6%8D%A2%E7%AC%AC%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%85%83%E7%B4%A0)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 类型
### 索引数组   
带有数字索引的数组  
```php
$cars=array("Volvo","BMW","SAAB");

// anathor ways
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="SAAB";
```
<br>[⬆ Back to top](#table-of-contents)

### 关联数组
使用您分配给数组的指定键的数组。  
```php
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

// another ways
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```
<br>[⬆ Back to top](#table-of-contents)

### 多维数组
包含一个或多个数组的数组。  
```php
$cars = array
  (
  array("Volvo",22,18),
  array("BMW",15,13),
  );

// another ways
$cars[0][0] = 'Volvo' ;
$cars[0][1] = 22;
$cars[0][2] = 18 ;
$cars[1][0] = 'BMW';
$cars[1][0] = 15;
$cars[1][0] = 13;
```
<br>[⬆ Back to top](#table-of-contents)

## 获取
### 输出数组中当前元素的值
**[current()](http://php.net/manual/zh/function.current.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo current($people); // 当前元素是 Bill
```
<br>[⬆ Back to top](#table-of-contents)

### 输出数组中最后一个元素的值
**[end()](http://php.net/manual/zh/function.end.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo end($people); // 最后一个元素是 David
```
<br>[⬆ Back to top](#table-of-contents)

### 输出数组中下一个元素的值
**[next()](http://php.net/manual/zh/function.next.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo next($people); // Bill 的下一个元素是 Steve
```
<br>[⬆ Back to top](#table-of-contents)

### 输出数组中上一个元素的值
**[prev()](http://php.net/manual/zh/function.prev.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo prev($people); // David 之前的元素是 Mark
```
<br>[⬆ Back to top](#table-of-contents)


### 输出数组中第一个元素的值
**[reset()](http://php.net/manual/zh/function.reset.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo reset($people); // 把内部指针移动到数组的首个元素，即 Bill
```
<br>[⬆ Back to top](#table-of-contents)

### 输出数组中当前元素的键名和键值，并将内部指针向前移动
**[each()](http://php.net/manual/zh/function.each.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

each($people); // 返回当前元素的键名和键值，即'0'=> Bill
echo current($people); // 并将内部指针向前移动, 即Steve
```
<br>[⬆ Back to top](#table-of-contents)

### 输出数组中当前元素键名
**[key()](http://php.net/manual/zh/function.key.php)**
```php
$a = array('key'=>'value');

echo key($a); // key
```
<br>[⬆ Back to top](#table-of-contents)

### 返回数组中部分的或所有的键名
**[array_keys()](返回数组中部分的或所有的键名)**
```php

$array = array(0 => 100, "color" => "red");

$result = array_keys($array);
print_r($result); // Array ( [0] => 0 [1] => color )
```
<br>[⬆ Back to top](#table-of-contents)

### 返回数组中所有的值
**[array_values()](http://php.net/manual/zh/function.array-values.php)**
```php

$array = array("size" => "XL", "color" => "gold");

$result = array_values($array);
print_r($result); // Array ( [0] => XL [1] => gold )
```
<br>[⬆ Back to top](#table-of-contents)

### 返回数组中指定的一列
**[array_column()](http://php.net/manual/zh/function.array-column.php)**
```php
// Array representing a possible record set returned from a database
$records = array(
    array(
        'id' => 2135,
        'first_name' => 'John',
        'last_name' => 'Doe',
    ),
    array(
        'id' => 3245,
        'first_name' => 'Sally',
        'last_name' => 'Smith',
    ),
    array(
        'id' => 5342,
        'first_name' => 'Jane',
        'last_name' => 'Jones',
    ),
    array(
        'id' => 5623,
        'first_name' => 'Peter',
        'last_name' => 'Doe',
    )
);

$first_names = array_column($records, 'first_name');
print_r($first_names); // Array ( [0] => John [1] => Sally [2] => Jane [3] => Peter )
```
<br>[⬆ Back to top](#table-of-contents)

## 操作
### 将数组中的所有键名修改为全大写或小写
**[array_change_key_case()](http://php.net/manual/zh/function.array-change-key-case.php)**
```php

$input_array = array("FirSt" => 1, "SecOnd" => 4);

// upper
$case_upper = array_change_key_case($input_array, CASE_UPPER);
print_r($case_upper); // Array ( [FIRST] => 1 [SECOND] => 4 ) 
// lower
$case_lower= array_change_key_case($input_array, CASE_LOWER);
print_r($case_lower); // Array ( [first] => 1 [second] => 4 )
```
<br>[⬆ Back to top](#table-of-contents)

### 从数组中取出一段
**[array_slice()](http://php.net/manual/zh/function.array-slice.php)**
```php
$input = array("a", "b", "c", "d", "e");

$output = array_slice($input, 2);      // returns "c", "d", and "e"
$output = array_slice($input, -2, 1);  // returns "d"
$output = array_slice($input, 0, 3);   // returns "a", "b", and "c"
```
<br>[⬆ Back to top](#table-of-contents)

### 把数组中的值赋给一组变量
**[list()](http://php.net/manual/zh/function.list.php)**
```php
$info = array('coffee', 'brown', 'caffeine');

list($drink, $color, $power) = $info;
echo "$drink is $color and $power makes it special."; // coffee is brown and caffeine makes it special.
```
<br>[⬆ Back to top](#table-of-contents)

### 建立一个包含指定范围单元的数组
**[range()](http://php.net/manual/zh/function.range.php)**
```php
$number = range(0, 5);
print_r($number); // Array ( [0] => 0 [1] => 1 [2] => 2 [3] => 3 [4] => 4 [5] => 5 ) 
```
<br>[⬆ Back to top](#table-of-contents)

### 打乱数组
**[shuffle](http://php.net/manual/zh/function.shuffle.php)**
```php
$number = range(0, 5);

shuffle($number);
print_r($number); //  Array ( [0] => 2 [1] => 4 [2] => 0 [3] => 5 [4] => 3 [5] => 1 ) 
```
<br>[⬆ Back to top](#table-of-contents)

### 移除数组中重复的值
**[array_unique()](http://php.net/manual/zh/function.array-unique.php)**
```php
$array = array(1, "hello", 1, "world", "hello");

$result = array_unique($array);
print_r($result); // Array ( [0] => 1 [1] => hello [3] => world )
```
<br>[⬆ Back to top](#table-of-contents)

### 创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值
**[array_combine()](http://php.net/manual/zh/function.array-combine.php)**
```php
$a = array('green', 'red', 'yellow');
$b = array('avocado', 'apple', 'banana');

$c = array_combine($a, $b);
print_r($c); // Array ( [green] => avocado [red] => apple [yellow] => banana )
```
<br>[⬆ Back to top](#table-of-contents)

### 创建包含变量名和它们的值的数组
**[compact()[http://php.net/manual/zh/function.compact.php)**
```php
$firstname = "Bill";
$lastname = "Gates";
$age = "60";

$result = compact("firstname", "lastname", "age");

print_r($result); // Array ( [firstname] => Bill [lastname] => Gates [age] => 60 )
```
<br>[⬆ Back to top](#table-of-contents)

### 从数组中将变量导入到当前的符号表
**[extract()](http://php.net/manual/zh/function.extract.php)**
```php
$var_array = array("color" => "blue",
                   "size"  => "medium",
                   "shape" => "sphere");
extract($var_array);

echo "$color, $size, $shape"; // blue, medium, sphere
```
<br>[⬆ Back to top](#table-of-contents)

## 排序
### 对数组排序,由低到高
**[sort()](http://php.net/manual/zh/function.sort.php)**
```php
// Array to be sorted
$fruits = array("lemon", "orange", "banana", "apple");

// Sort and print the resulting array
sort($fruits);
print_r($fruits); //  Array ( [0] => apple [1] => banana [2] => lemon [3] => orange )
```
<br>[⬆ Back to top](#table-of-contents)

### 对数组逆向排序,由高到低
**[rsort()](http://php.net/manual/zh/function.rsort.php)**
```php
// Array to be sorted
$fruits = array("lemon", "orange", "banana", "apple");

// Sort and print the resulting array
rsort($fruits);
print_r($fruits); // Array ( [0] => orange [1] => lemon [2] => banana [3] => apple )
```
<br>[⬆ Back to top](#table-of-contents)

### 对数组按照键名排序,由低到高
**[ksort()](http://php.net/manual/zh/function.ksort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
ksort($fruits);
print_r($fruits); // Array ( [a] => orange [b] => banana [c] => apple [d] => lemon )
```
<br>[⬆ Back to top](#table-of-contents)

### 对数组按照键名逆向排序,由高到低
**[krsort()](http://php.net/manual/zh/function.krsort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
krsort($fruits);
print_r($fruits); // Array ( [d] => lemon [c] => apple [b] => banana [a] => orange )
```
<br>[⬆ Back to top](#table-of-contents)

###  对数组进行排序并保持索引关系,由低到高
**[asort()](http://php.net/manual/zh/function.asort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
asort($fruits);
print_r($fruits); // Array ( [c] => apple [b] => banana [d] => lemon [a] => orange )
```
<br>[⬆ Back to top](#table-of-contents)

### 对数组进行逆向排序并保持索引关系,由高到低
**[arsort()](http://php.net/manual/zh/function.arsort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
arsort($fruits);
print_r($fruits); // Array ( [a] => orange [d] => lemon [b] => banana [c] => apple )
```
<br>[⬆ Back to top](#table-of-contents)

### 使用用户自定义的比较函数对数组中的值进行排序
**[usort()](http://php.net/manual/zh/function.usort.php)**
```php
function cmp($a, $b)
{
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Array to be sorted
$a = array(3, 2, 5, 6, 1);

// Sort and print the resulting array
usort($a, "cmp");
print_r($a); // Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 5 [4] => 6 )
```
<br>[⬆ Back to top](#table-of-contents)

### 使用用户自定义的比较函数对数组中的值进行排序并保持索引关联
**[uasort()](http://php.net/manual/zh/function.uasort.php)**
```php
function cmp($a, $b)
{
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Array to be sorted
$array = array('a' => 4, 'b' => 8, 'c' => -1, 'd' => -9, 'e' => 2, 'f' => 5, 'g' => 3, 'h' => -4);

// Sort and print the resulting array
uasort($array, 'cmp');
print_r($array); // Array ( [d] => -9 [h] => -4 [c] => -1 [e] => 2 [g] => 3 [a] => 4 [f] => 5 [b] => 8 )
```
<br>[⬆ Back to top](#table-of-contents)

### 使用用户自定义的比较函数对数组中的键名进行排序
**[uksort()](http://php.net/manual/zh/function.uksort.php)**
```php
function cmp($a, $b)
{
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Array to be sorted
$array = array('f' => 5, 'a' => 4, 'h' => -4, 'd' => -9, 'c' => -1, 'e' => 2, 'g' => 3, 'b' => 8);

// Sort and print the resulting array
uksort($array, 'cmp');
print_r($array); // Array ( [a] => 4 [b] => 8 [c] => -1 [d] => -9 [e] => 2 [f] => 5 [g] => 3 [h] => -4 )
```
<br>[⬆ Back to top](#table-of-contents)

### 用“自然排序”算法对数组排序
**[natsort()](http://php.net/manual/zh/function.natsort.php)**
```php
// Array to be sorted
$array1 = $array2 = array("img12.png", "img10.png", "img2.png", "img1.png");

// Standard sorting
asort($array1);
print_r($array1); //  Array ( [3] => img1.png [1] => img10.png [0] => img12.png [2] => img2.png ) 

//nNatural order sorting
natsort($array2);
print_r($array2); // Array ( [3] => img1.png [2] => img2.png [1] => img10.png [0] => img12.png )
```
<br>[⬆ Back to top](#table-of-contents)

### 用“自然排序”算法对数组进行不区分大小写字母的排序
**[natcasesort()](http://php.net/manual/zh/function.natcasesort.php)**
```php
// Array to be sorted
$array1 = $array2 = array('IMG0.png', 'img12.png', 'img10.png', 'img2.png', 'img1.png', 'IMG3.png');

// Standard sorting
sort($array1);
print_r($array1);
// Array ( [0] => IMG0.png [1] => IMG3.png [2] => img1.png [3] => img10.png [4] => img12.png [5] => img2.png )

// nNatural order sorting (case-insensitive)
natcasesort($array2);
print_r($array2); 
// Array ( [0] => IMG0.png [4] => img1.png [3] => img2.png [5] => IMG3.png [2] => img10.png [1] => img12.png )
```
<br>[⬆ Back to top](#table-of-contents)

## 统计检查
### 统计数组中元素数量
**[count()](http://php.net/manual/zh/function.count.php)**
```php
$a = array(0,1,2,3);

echo count($a); // 4
```
<br>[⬆ Back to top](#table-of-contents)

### 统计数组中所有的值
**[array_count_values()](http://php.net/manual/zh/function.array-count-values.php)**
```php
$array = array(1, "hello", 1, "world", "hello");

$result = array_count_values($array);
print_r($result); // Array ( [1] => 2 [hello] => 2 [world] => 1 )
```
<br>[⬆ Back to top](#table-of-contents)

### 检查数组里是否有指定的键名或索引
**[array_key_exists()](http://php.net/manual/zh/function.array-key-exists.php)**
```php
$search_array = array('first' => 1, 'second' => 4);
echo array_key_exists('first', $search_array); // 1
```
<br>[⬆ Back to top](#table-of-contents)

### 检查数组中是否存在某个值
**[in_array()](http://php.net/manual/zh/function.in-array.php)**
```php
$os = array("Mac", "NT", "Irix", "Linux");
echo in_array("Irix", $os); // 1
```
<br>[⬆ Back to top](#table-of-contents)

## 分割合并替换
### 将一个数组分割成多个
**[array_chunk()](http://php.net/manual/zh/function.array-chunk.php)**
```php
$input_array = array('a', 'b', 'c', 'd', 'e');

$output_array = array_chunk($input_array, 2);
print_r($output_array);
// Array ( [0] => Array ( [0] => a [1] => b ) [1] => Array ( [0] => c [1] => d ) [2] => Array ( [0] => e ) )
```
<br>[⬆ Back to top](#table-of-contents)

### 合并一个或多个数组
**[array_merge()](http://php.net/manual/zh/function.array-merge.php)**
```php
$array1 = array("color" => "red", 2, 4);
$array2 = array("a", "b", "color" => "green", "shape" => "trapezoid", 4);

$result = array_merge($array1, $array2);
print_r($result); // Array ( [color] => green [0] => 2 [1] => 4 [2] => a [3] => b [shape] => trapezoid [4] => 4 )
```
<br>[⬆ Back to top](#table-of-contents)

### 递归地合并一个或多个数组
**[array_merge_recursive()](http://php.net/manual/zh/function.array-merge-recursive.php)**
```php
$ar1 = array("color" => array("favorite" => "red"), 5);
$ar2 = array(10, "color" => array("favorite" => "green", "blue"));

$result = array_merge_recursive($ar1, $ar2);
print_r($result); // Array ( [color] => Array ( [favorite] => Array ( [0] => red [1] => green ) [0] => blue ) [0] => 5 [1] => 10 )
```
<br>[⬆ Back to top](#table-of-contents)

### 使用传递的数组替换第一个数组的元素
**[array_replace()](http://php.net/manual/zh/function.array-replace.php)**
```php
$base = array("orange", "banana", "apple", "raspberry");
$replacements = array(0 => "pineapple", 4 => "cherry");
$replacements2 = array(0 => "grape");

$basket = array_replace($base, $replacements, $replacements2);
print_r($basket); // Array ( [0] => grape [1] => banana [2] => apple [3] => raspberry [4] => cherry )
```
<br>[⬆ Back to top](#table-of-contents)

### 使用传递的数组递归替换第一个数组的元素
**[array_replace_recursive()](http://php.net/manual/zh/function.array-replace-recursive.php)**
```php
$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );
$replacements = array('citrus' => array('pineapple'), 'berries' => array('blueberry'));

$basket = array_replace_recursive($base, $replacements);
print_r($basket); // Array ( [citrus] => Array ( [0] => pineapple ) [berries] => Array ( [0] => blueberry [1] => raspberry ) 

$basket = array_replace($base, $replacements);
print_r($basket); // Array ( [citrus] => Array ( [0] => pineapple ) [berries] => Array ( [0] => blueberry ) )
```
<br>[⬆ Back to top](#table-of-contents)

