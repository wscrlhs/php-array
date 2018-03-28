## 收藏的PHP数组函数
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## 目录

- [类型](#%E7%B1%BB%E5%9E%8B)
  - [索引数组](#%E7%B4%A2%E5%BC%95%E6%95%B0%E7%BB%84)
  - [关联数组](#%E5%85%B3%E8%81%94%E6%95%B0%E7%BB%84)
  - [多维数组](#%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84)
- [取值](#%E5%8F%96%E5%80%BC)
  - [输出数组中当前元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中最后一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中下一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中上一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E4%B8%8A%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中第一个元素的值](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%85%83%E7%B4%A0%E7%9A%84%E5%80%BC)
  - [输出数组中当前元素的键名和键值，并将内部指针向前移动](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E7%9A%84%E9%94%AE%E5%90%8D%E5%92%8C%E9%94%AE%E5%80%BC%E5%B9%B6%E5%B0%86%E5%86%85%E9%83%A8%E6%8C%87%E9%92%88%E5%90%91%E5%89%8D%E7%A7%BB%E5%8A%A8)
  - [输出数组中当前元素键名](#%E8%BE%93%E5%87%BA%E6%95%B0%E7%BB%84%E4%B8%AD%E5%BD%93%E5%89%8D%E5%85%83%E7%B4%A0%E9%94%AE%E5%90%8D)
  - [返回数组中部分的或所有的键名](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E9%83%A8%E5%88%86%E7%9A%84%E6%88%96%E6%89%80%E6%9C%89%E7%9A%84%E9%94%AE%E5%90%8D)
  - [返回数组中所有的值](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E7%9A%84%E5%80%BC)
  - [返回单元顺序相反的数组](#%E8%BF%94%E5%9B%9E%E5%8D%95%E5%85%83%E9%A1%BA%E5%BA%8F%E7%9B%B8%E5%8F%8D%E7%9A%84%E6%95%B0%E7%BB%84)
  - [返回数组中指定的一列](#%E8%BF%94%E5%9B%9E%E6%95%B0%E7%BB%84%E4%B8%AD%E6%8C%87%E5%AE%9A%E7%9A%84%E4%B8%80%E5%88%97)
  - [从数组中随机取出一个或多个单元](#%E4%BB%8E%E6%95%B0%E7%BB%84%E4%B8%AD%E9%9A%8F%E6%9C%BA%E5%8F%96%E5%87%BA%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E5%8D%95%E5%85%83)
- [操作](#%E6%93%8D%E4%BD%9C)
  - [将数组中的所有键名修改为全大写或小写](#%E5%B0%86%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%89%80%E6%9C%89%E9%94%AE%E5%90%8D%E4%BF%AE%E6%94%B9%E4%B8%BA%E5%85%A8%E5%A4%A7%E5%86%99%E6%88%96%E5%B0%8F%E5%86%99)
  - [从数组中取出一段](#%E4%BB%8E%E6%95%B0%E7%BB%84%E4%B8%AD%E5%8F%96%E5%87%BA%E4%B8%80%E6%AE%B5)
  - [把数组中的值赋给一组变量](#%E6%8A%8A%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E5%80%BC%E8%B5%8B%E7%BB%99%E4%B8%80%E7%BB%84%E5%8F%98%E9%87%8F)
  - [建立一个包含指定范围单元的数组](#%E5%BB%BA%E7%AB%8B%E4%B8%80%E4%B8%AA%E5%8C%85%E5%90%AB%E6%8C%87%E5%AE%9A%E8%8C%83%E5%9B%B4%E5%8D%95%E5%85%83%E7%9A%84%E6%95%B0%E7%BB%84)
  - [去掉数组中的某一部分并用其它值取代](#%E5%8E%BB%E6%8E%89%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%9F%90%E4%B8%80%E9%83%A8%E5%88%86%E5%B9%B6%E7%94%A8%E5%85%B6%E5%AE%83%E5%80%BC%E5%8F%96%E4%BB%A3)
  - [在数组中搜索给定的值，如果成功则返回首个相应的键名](#%E5%9C%A8%E6%95%B0%E7%BB%84%E4%B8%AD%E6%90%9C%E7%B4%A2%E7%BB%99%E5%AE%9A%E7%9A%84%E5%80%BC%E5%A6%82%E6%9E%9C%E6%88%90%E5%8A%9F%E5%88%99%E8%BF%94%E5%9B%9E%E9%A6%96%E4%B8%AA%E7%9B%B8%E5%BA%94%E7%9A%84%E9%94%AE%E5%90%8D)
  - [打乱数组](#%E6%89%93%E4%B9%B1%E6%95%B0%E7%BB%84)
  - [移除数组中重复的值](#%E7%A7%BB%E9%99%A4%E6%95%B0%E7%BB%84%E4%B8%AD%E9%87%8D%E5%A4%8D%E7%9A%84%E5%80%BC)
  - [将一个数组分割成多个](#%E5%B0%86%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E5%88%86%E5%89%B2%E6%88%90%E5%A4%9A%E4%B8%AA)
  - [交换数组中的键和值](#%E4%BA%A4%E6%8D%A2%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E9%94%AE%E5%92%8C%E5%80%BC)
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
  - [对多个数组或多维数组进行排序](#%E5%AF%B9%E5%A4%9A%E4%B8%AA%E6%95%B0%E7%BB%84%E6%88%96%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F)
- [计算](#%E8%AE%A1%E7%AE%97)
  - [统计数组中元素数量](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E4%B8%AD%E5%85%83%E7%B4%A0%E6%95%B0%E9%87%8F)
  - [统计数组中所有的值](#%E7%BB%9F%E8%AE%A1%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E7%9A%84%E5%80%BC)
  - [对数组中所有值求和](#%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E5%80%BC%E6%B1%82%E5%92%8C)
  - [计算数组中所有值的乘积](#%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E4%B8%AD%E6%89%80%E6%9C%89%E5%80%BC%E7%9A%84%E4%B9%98%E7%A7%AF)
- [检查](#%E6%A3%80%E6%9F%A5)
  - [检查数组里是否有指定的键名或索引](#%E6%A3%80%E6%9F%A5%E6%95%B0%E7%BB%84%E9%87%8C%E6%98%AF%E5%90%A6%E6%9C%89%E6%8C%87%E5%AE%9A%E7%9A%84%E9%94%AE%E5%90%8D%E6%88%96%E7%B4%A2%E5%BC%95)
  - [检查数组中是否存在某个值](#%E6%A3%80%E6%9F%A5%E6%95%B0%E7%BB%84%E4%B8%AD%E6%98%AF%E5%90%A6%E5%AD%98%E5%9C%A8%E6%9F%90%E4%B8%AA%E5%80%BC)
- [合并](#%E5%90%88%E5%B9%B6)
  - [合并一个或多个数组](#%E5%90%88%E5%B9%B6%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E6%95%B0%E7%BB%84)
  - [递归地合并一个或多个数组](#%E9%80%92%E5%BD%92%E5%9C%B0%E5%90%88%E5%B9%B6%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E6%95%B0%E7%BB%84)
- [替换](#%E6%9B%BF%E6%8D%A2)
  - [使用传递的数组替换第一个数组的元素](#%E4%BD%BF%E7%94%A8%E4%BC%A0%E9%80%92%E7%9A%84%E6%95%B0%E7%BB%84%E6%9B%BF%E6%8D%A2%E7%AC%AC%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%85%83%E7%B4%A0)
  - [使用传递的数组递归替换第一个数组的元素](#%E4%BD%BF%E7%94%A8%E4%BC%A0%E9%80%92%E7%9A%84%E6%95%B0%E7%BB%84%E9%80%92%E5%BD%92%E6%9B%BF%E6%8D%A2%E7%AC%AC%E4%B8%80%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E5%85%83%E7%B4%A0)
- [填充](#%E5%A1%AB%E5%85%85)
  - [使用指定的键和值填充数组](#%E4%BD%BF%E7%94%A8%E6%8C%87%E5%AE%9A%E7%9A%84%E9%94%AE%E5%92%8C%E5%80%BC%E5%A1%AB%E5%85%85%E6%95%B0%E7%BB%84)
  - [用给定的值填充数组](#%E7%94%A8%E7%BB%99%E5%AE%9A%E7%9A%84%E5%80%BC%E5%A1%AB%E5%85%85%E6%95%B0%E7%BB%84)
  - [以指定长度将一个值填充进数组](#%E4%BB%A5%E6%8C%87%E5%AE%9A%E9%95%BF%E5%BA%A6%E5%B0%86%E4%B8%80%E4%B8%AA%E5%80%BC%E5%A1%AB%E5%85%85%E8%BF%9B%E6%95%B0%E7%BB%84)
- [堆栈](#%E5%A0%86%E6%A0%88)
  - [将数组开头的单元移出数组](#%E5%B0%86%E6%95%B0%E7%BB%84%E5%BC%80%E5%A4%B4%E7%9A%84%E5%8D%95%E5%85%83%E7%A7%BB%E5%87%BA%E6%95%B0%E7%BB%84)
  - [在数组开头插入一个或多个单元](#%E5%9C%A8%E6%95%B0%E7%BB%84%E5%BC%80%E5%A4%B4%E6%8F%92%E5%85%A5%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E5%8D%95%E5%85%83)
  - [弹出数组最后一个单元（出栈）](#%E5%BC%B9%E5%87%BA%E6%95%B0%E7%BB%84%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E5%8D%95%E5%85%83%E5%87%BA%E6%A0%88)
  - [将一个或多个单元压入数组的末尾（入栈）](#%E5%B0%86%E4%B8%80%E4%B8%AA%E6%88%96%E5%A4%9A%E4%B8%AA%E5%8D%95%E5%85%83%E5%8E%8B%E5%85%A5%E6%95%B0%E7%BB%84%E7%9A%84%E6%9C%AB%E5%B0%BE%E5%85%A5%E6%A0%88)
- [回调](#%E5%9B%9E%E8%B0%83)
  - [使用用户自定义函数对数组中的每个元素做回调处理](#%E4%BD%BF%E7%94%A8%E7%94%A8%E6%88%B7%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%AF%8F%E4%B8%AA%E5%85%83%E7%B4%A0%E5%81%9A%E5%9B%9E%E8%B0%83%E5%A4%84%E7%90%86)
  - [对数组中的每个成员递归地应用用户函数](#%E5%AF%B9%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E6%AF%8F%E4%B8%AA%E6%88%90%E5%91%98%E9%80%92%E5%BD%92%E5%9C%B0%E5%BA%94%E7%94%A8%E7%94%A8%E6%88%B7%E5%87%BD%E6%95%B0)
  - [为数组的每个元素应用回调函数](#%E4%B8%BA%E6%95%B0%E7%BB%84%E7%9A%84%E6%AF%8F%E4%B8%AA%E5%85%83%E7%B4%A0%E5%BA%94%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0)
  - [用回调函数迭代地将数组简化为单一的值](#%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E8%BF%AD%E4%BB%A3%E5%9C%B0%E5%B0%86%E6%95%B0%E7%BB%84%E7%AE%80%E5%8C%96%E4%B8%BA%E5%8D%95%E4%B8%80%E7%9A%84%E5%80%BC)
  - [用回调函数过滤数组中的单元](#%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E8%BF%87%E6%BB%A4%E6%95%B0%E7%BB%84%E4%B8%AD%E7%9A%84%E5%8D%95%E5%85%83)
- [差集](#%E5%B7%AE%E9%9B%86)
  - [计算数组的差集](#%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
  - [用回调函数比较数据来计算数组的差集](#%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE%E6%9D%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
  - [带索引检查计算数组的差集](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
  - [用用户提供的回调函数做索引检查来计算数组的差集](#%E7%94%A8%E7%94%A8%E6%88%B7%E6%8F%90%E4%BE%9B%E7%9A%84%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E5%81%9A%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E6%9D%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
  - [带索引检查计算数组的差集，用回调函数比较数据](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE)
  - [带索引检查计算数组的差集，用回调函数比较数据和索引](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE%E5%92%8C%E7%B4%A2%E5%BC%95)
  - [使用键名比较计算数组的差集](#%E4%BD%BF%E7%94%A8%E9%94%AE%E5%90%8D%E6%AF%94%E8%BE%83%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
  - [用回调函数对键名比较计算数组的差集](#%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E5%AF%B9%E9%94%AE%E5%90%8D%E6%AF%94%E8%BE%83%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E5%B7%AE%E9%9B%86)
- [交集](#%E4%BA%A4%E9%9B%86)
  - [计算数组的交集](#%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86)
  - [计算数组的交集，用回调函数比较数据](#%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE)
  - [带索引检查计算数组的交集](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86)
  - [带索引检查计算数组的交集，用回调函数比较索引](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E7%B4%A2%E5%BC%95)
  - [带索引检查计算数组的交集，用回调函数比较数据](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE)
  - [带索引检查计算数组的交集，用单独的回调函数比较数据和索引](#%E5%B8%A6%E7%B4%A2%E5%BC%95%E6%A3%80%E6%9F%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86%E7%94%A8%E5%8D%95%E7%8B%AC%E7%9A%84%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E6%95%B0%E6%8D%AE%E5%92%8C%E7%B4%A2%E5%BC%95)
  - [使用键名比较计算数组的交集](#%E4%BD%BF%E7%94%A8%E9%94%AE%E5%90%8D%E6%AF%94%E8%BE%83%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86)
  - [用回调函数比较键名来计算数组的交集](#%E7%94%A8%E5%9B%9E%E8%B0%83%E5%87%BD%E6%95%B0%E6%AF%94%E8%BE%83%E9%94%AE%E5%90%8D%E6%9D%A5%E8%AE%A1%E7%AE%97%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 类型
### 索引数组
带有数字索引的数组
```php
$cars=array("Volvo","BMW","SAAB");

// anothor ways
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="SAAB";
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 关联数组
使用您分配给数组的指定键的数组。
```php
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

// another ways
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 取值
### 输出数组中当前元素的值
**[current()](http://php.net/manual/zh/function.current.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo current($people); // 当前元素是 Bill
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 输出数组中最后一个元素的值
**[end()](http://php.net/manual/zh/function.end.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo end($people); // 最后一个元素是 David
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 输出数组中下一个元素的值
**[next()](http://php.net/manual/zh/function.next.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo next($people); // Bill 的下一个元素是 Steve
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 输出数组中上一个元素的值
**[prev()](http://php.net/manual/zh/function.prev.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo prev($people); // David 之前的元素是 Mark
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


### 输出数组中第一个元素的值
**[reset()](http://php.net/manual/zh/function.reset.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

echo reset($people); // 把内部指针移动到数组的首个元素，即 Bill
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 输出数组中当前元素的键名和键值，并将内部指针向前移动
**[each()](http://php.net/manual/zh/function.each.php)**
```php
$people = array("Bill", "Steve", "Mark", "David");

each($people); // 返回当前元素的键名和键值，即'0'=> Bill
echo current($people); // 并将内部指针向前移动, 即Steve
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 输出数组中当前元素键名
**[key()](http://php.net/manual/zh/function.key.php)**
```php
$a = array('key'=>'value');

echo key($a); // key
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 返回数组中部分的或所有的键名
**[array_keys()](返回数组中部分的或所有的键名)**
```php

$array = array(0 => 100, "color" => "red");

$result = array_keys($array);
print_r($result); // Array ( [0] => 0 [1] => color )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 返回数组中所有的值
**[array_values()](http://php.net/manual/zh/function.array-values.php)**
```php

$array = array("size" => "XL", "color" => "gold");

$result = array_values($array);
print_r($result); // Array ( [0] => XL [1] => gold )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 返回单元顺序相反的数组
**[array_reverse()](http://php.net/manual/zh/function.array-reverse.php)**
```php
$input  = array("php", 4.0, array("green", "red"));

$reversed = array_reverse($input);
print_r($reversed); // Array ( [0] => Array ( [0] => green [1] => red ) [1] => 4 [2] => php )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 从数组中随机取出一个或多个单元
**[array_rand()](http://php.net/manual/zh/function.array-rand.php)**
```php
$input = array("Neo", "Morpheus", "Trinity", "Cypher", "Tank");

$rand_keys = array_rand($input, 2);
print_r($rand_keys); // Array ( [0] => 2 [1] => 4 )
echo $input[$rand_keys[0]]; // Neo
echo $input[$rand_keys[1]]; // Tank
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 从数组中取出一段
**[array_slice()](http://php.net/manual/zh/function.array-slice.php)**
```php
$input = array("a", "b", "c", "d", "e");

$output = array_slice($input, 2);      // returns "c", "d", and "e"
$output = array_slice($input, -2, 1);  // returns "d"
$output = array_slice($input, 0, 3);   // returns "a", "b", and "c"
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 把数组中的值赋给一组变量
**[list()](http://php.net/manual/zh/function.list.php)**
```php
$info = array('coffee', 'brown', 'caffeine');

list($drink, $color, $power) = $info;
echo "$drink is $color and $power makes it special."; // coffee is brown and caffeine makes it special.
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 建立一个包含指定范围单元的数组
**[range()](http://php.net/manual/zh/function.range.php)**
```php
$number = range(0, 5);
print_r($number); // Array ( [0] => 0 [1] => 1 [2] => 2 [3] => 3 [4] => 4 [5] => 5 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 去掉数组中的某一部分并用其它值取代
**[array_splice()](http://php.net/manual/zh/function.array-splice.php)**
```php
$input = array("red", "green", "blue", "yellow");

array_splice($input, 1, 1, "orange");
print_r($input); //Array ( [0] => red [1] => orange [2] => blue [3] => yellow )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 在数组中搜索给定的值，如果成功则返回首个相应的键名
**[array_search()](http://php.net/manual/zh/function.array-search.php)**
```php
$array = array(0 => 'blue', 1 => 'red', 2 => 'green', 3 => 'red');

$key = array_search('green', $array);
print_r($key); // 2
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 打乱数组
**[shuffle](http://php.net/manual/zh/function.shuffle.php)**
```php
$number = range(0, 5);

shuffle($number);
print_r($number); //  Array ( [0] => 2 [1] => 4 [2] => 0 [3] => 5 [4] => 3 [5] => 1 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 移除数组中重复的值
**[array_unique()](http://php.net/manual/zh/function.array-unique.php)**
```php
$array = array(1, "hello", 1, "world", "hello");

$result = array_unique($array);
print_r($result); // Array ( [0] => 1 [1] => hello [3] => world )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 将一个数组分割成多个
**[array_chunk()](http://php.net/manual/zh/function.array-chunk.php)**
```php
$input_array = array('a', 'b', 'c', 'd', 'e');

$output_array = array_chunk($input_array, 2);
print_r($output_array);
// Array ( [0] => Array ( [0] => a [1] => b ) [1] => Array ( [0] => c [1] => d ) [2] => Array ( [0] => e ) )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 交换数组中的键和值
**[array_flip()](http://php.net/manual/zh/function.array-flip.php)**
```php
$input = array("oranges", "apples", "pears");

$flipped = array_flip($input);
print_r($flipped); // Array ( [oranges] => 0 [apples] => 1 [pears] => 2 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


### 创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值
**[array_combine()](http://php.net/manual/zh/function.array-combine.php)**
```php
$a = array('green', 'red', 'yellow');
$b = array('avocado', 'apple', 'banana');

$c = array_combine($a, $b);
print_r($c); // Array ( [green] => avocado [red] => apple [yellow] => banana )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 创建包含变量名和它们的值的数组
**[compact()](http://php.net/manual/zh/function.compact.php)**
```php
$firstname = "Bill";
$lastname = "Gates";
$age = "60";

$result = compact("firstname", "lastname", "age");

print_r($result); // Array ( [firstname] => Bill [lastname] => Gates [age] => 60 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 从数组中将变量导入到当前的符号表
**[extract()](http://php.net/manual/zh/function.extract.php)**
```php
$var_array = array("color" => "blue",
                   "size"  => "medium",
                   "shape" => "sphere");
extract($var_array);

echo "$color, $size, $shape"; // blue, medium, sphere
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组逆向排序,由高到低
**[rsort()](http://php.net/manual/zh/function.rsort.php)**
```php
// Array to be sorted
$fruits = array("lemon", "orange", "banana", "apple");

// Sort and print the resulting array
rsort($fruits);
print_r($fruits); // Array ( [0] => orange [1] => lemon [2] => banana [3] => apple )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组按照键名排序,由低到高
**[ksort()](http://php.net/manual/zh/function.ksort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
ksort($fruits);
print_r($fruits); // Array ( [a] => orange [b] => banana [c] => apple [d] => lemon )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组按照键名逆向排序,由高到低
**[krsort()](http://php.net/manual/zh/function.krsort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
krsort($fruits);
print_r($fruits); // Array ( [d] => lemon [c] => apple [b] => banana [a] => orange )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

###  对数组进行排序并保持索引关系,由低到高
**[asort()](http://php.net/manual/zh/function.asort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
asort($fruits);
print_r($fruits); // Array ( [c] => apple [b] => banana [d] => lemon [a] => orange )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组进行逆向排序并保持索引关系,由高到低
**[arsort()](http://php.net/manual/zh/function.arsort.php)**
```php
// Array to be sorted
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");

// Sort and print the resulting array
arsort($fruits);
print_r($fruits); // Array ( [a] => orange [d] => lemon [b] => banana [c] => apple )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对多个数组或多维数组进行排序
**[array_multisort()](http://php.net/manual/zh/function.array-multisort.php)**
```php
$arr = array(
    array(
        'top' => 0,
        'cnt' => 20,
    ),
    array(
        'top' => 0,
        'cnt' => 10,
    ),
    array(
        'top' => 1,
        'cnt' => 30,
    ),
);

array_multisort(array_column($arr, 'top'), SORT_DESC, SORT_NUMERIC,
    array_column($arr, 'cnt'), SORT_ASC, SORT_NUMERIC,
    $arr);
print_r($arr); // Array ( [0] => Array ( [top] => 1 [cnt] => 30 ) [1] => Array ( [top] => 0 [cnt] => 10 ) [2] => Array ( [top] => 0 [cnt] => 20 ) )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 计算
### 统计数组中元素数量
**[count()](http://php.net/manual/zh/function.count.php)**
```php
$a = array(0,1,2,3);

echo count($a); // 4
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 统计数组中所有的值
**[array_count_values()](http://php.net/manual/zh/function.array-count-values.php)**
```php
$array = array(1, "hello", 1, "world", "hello");

$result = array_count_values($array);
print_r($result); // Array ( [1] => 2 [hello] => 2 [world] => 1 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组中所有值求和
**[array_sum()](http://php.net/manual/zh/function.array-sum.php)**
```php

$a = array(2, 4, 6, 8);
$sum = array_sum($a);
echo "sum(a) = " . $sum; // sum(a) = 20
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 计算数组中所有值的乘积
**[array_product()](http://php.net/manual/zh/function.array-product.php)**
```php
$a = array(2, 4, 6, 8);

$result = array_product($a);
print_r($result); // 384
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


## 检查
### 检查数组里是否有指定的键名或索引
**[array_key_exists()](http://php.net/manual/zh/function.array-key-exists.php)**
```php
$search_array = array('first' => 1, 'second' => 4);
echo array_key_exists('first', $search_array); // 1
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 检查数组中是否存在某个值
**[in_array()](http://php.net/manual/zh/function.in-array.php)**
```php
$os = array("Mac", "NT", "Irix", "Linux");
echo in_array("Irix", $os); // 1
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 合并
### 合并一个或多个数组
**[array_merge()](http://php.net/manual/zh/function.array-merge.php)**
```php
$array1 = array("color" => "red", 2, 4);
$array2 = array("a", "b", "color" => "green", "shape" => "trapezoid", 4);

$result = array_merge($array1, $array2);
print_r($result); // Array ( [color] => green [0] => 2 [1] => 4 [2] => a [3] => b [shape] => trapezoid [4] => 4 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 递归地合并一个或多个数组
**[array_merge_recursive()](http://php.net/manual/zh/function.array-merge-recursive.php)**
```php
$ar1 = array("color" => array("favorite" => "red"), 5);
$ar2 = array(10, "color" => array("favorite" => "green", "blue"));

$result = array_merge_recursive($ar1, $ar2);
print_r($result); // Array ( [color] => Array ( [favorite] => Array ( [0] => red [1] => green ) [0] => blue ) [0] => 5 [1] => 10 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 替换
### 使用传递的数组替换第一个数组的元素
**[array_replace()](http://php.net/manual/zh/function.array-replace.php)**
```php
$base = array("orange", "banana", "apple", "raspberry");
$replacements = array(0 => "pineapple", 4 => "cherry");
$replacements2 = array(0 => "grape");

$basket = array_replace($base, $replacements, $replacements2);
print_r($basket); // Array ( [0] => grape [1] => banana [2] => apple [3] => raspberry [4] => cherry )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

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
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 填充
### 使用指定的键和值填充数组
**[array_fill_keys()]()**
```php

$keys = array('foo', 5, 10, 'bar');

$a = array_fill_keys($keys, 'banana');
print_r($a); // Array ( [foo] => banana [5] => banana [10] => banana [bar] => banana )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用给定的值填充数组
**[array_fill()]()**
```php
$a = array_fill(5, 3, 'banana');

print_r($a); // Array ( [5] => banana [6] => banana [7] => banana )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 以指定长度将一个值填充进数组
**[array_pad()]()**
```php
$input = array(12, 10, 9);

$result = array_pad($input, 5, 0);
print_r($result); // Array ( [0] => 12 [1] => 10 [2] => 9 [3] => 0 [4] => 0 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 堆栈
### 将数组开头的单元移出数组
**[array_shift()]()**
```php
stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_shift($stack);

print_r($stack); // Array ( [0] => banana [1] => apple [2] => raspberry )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 在数组开头插入一个或多个单元
**[array_unshift()]()**
```php
$queue = array("orange", "banana");
array_unshift($queue, "apple", "raspberry");

print_r($queue); // Array ( [0] => apple [1] => raspberry [2] => orange [3] => banana )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 弹出数组最后一个单元（出栈）
**[array_pop()]()**
```php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_pop($stack);

print_r($stack); // Array ( [0] => orange [1] => banana [2] => apple )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 将一个或多个单元压入数组的末尾（入栈）
**[array_push()]()**
```php
$stack = array("orange", "banana");
array_push($stack, "apple", "raspberry");

print_r($stack); // Array ( [0] => orange [1] => banana [2] => apple [3] => raspberry )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 回调
### 使用用户自定义函数对数组中的每个元素做回调处理
**[array_walk()]()**
```php
$fruits = array("d" => "lemon", "a" => "orange");

function test_alter(&$item1, $key, $prefix)
{
    $item1 = "$prefix: $item1";
}

array_walk($fruits, 'test_alter', 'fruit');
print_r($fruits); // Array ( [d] => fruit: lemon [a] => fruit: orange )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 对数组中的每个成员递归地应用用户函数
**[array_walk_recursive()]()**
```php
$sweet = array('a' => 'apple', 'b' => 'banana');
$fruits = array('sweet' => $sweet, 'sour' => 'lemon');

function test_alter(&$item1, $key, $prefix)
{
    $item1 = "$prefix: $item1";
}

array_walk_recursive($fruits, 'test_alter','fruit');
print_r($fruits); // Array ( [sweet] => Array ( [a] => fruit: apple [b] => fruit: banana ) [sour] => fruit: lemon )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 为数组的每个元素应用回调函数
**[array_map()]()**
```php

function cube($n)
{
    return($n * $n * $n);
}

$a = array(1, 2, 3, 4, 5);

$b = array_map("cube", $a);
print_r($b); // Array ( [0] => 1 [1] => 8 [2] => 27 [3] => 64 [4] => 125 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用回调函数迭代地将数组简化为单一的值
**[array_reduce()]()**
```php
function sum($carry, $item)
{
    $carry += $item;
    return $carry;
}

$a = array(1, 2, 3, 4, 5);

$result = array_reduce($a, "sum");
print_r($result); // 15
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用回调函数过滤数组中的单元
**[array_filter()]()**
```php
function odd($var)
{
    // returns whether the input integer is odd
    return($var & 1);
}

function even($var)
{
    // returns whether the input integer is even
    return(!($var & 1));
}

$array1 = array("a"=>1, "b"=>2, "c"=>3, "d"=>4, "e"=>5);
$array2 = array(6, 7, 8, 9, 10, 11, 12);

print_r(array_filter($array1, "odd")); //  Array ( [a] => 1 [c] => 3 [e] => 5 )
print_r(array_filter($array2, "even")); // Array ( [0] => 6 [2] => 8 [4] => 10 [6] => 12 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 差集
### 计算数组的差集
**[array_diff()]()**
```php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");

$result = array_diff($array1, $array2);
print_r($result); // Array ( [b] => brown [c] => blue )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用回调函数比较数据来计算数组的差集
**[array_udiff()]()**
```php
function value_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green",  "yellow", "red");
$result = array_udiff($array1, $array2, "value_compare_func");
print_r($result); // Array ( [b] => brown [c] => blue )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的差集
**[array_diff_assoc()]()**
```php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");

$result = array_diff_assoc($array1, $array2);
print_r($result); // Array ( [b] => brown [c] => blue [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用用户提供的回调函数做索引检查来计算数组的差集
**[array_diff_uassoc()]()**
```php
function key_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");

$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result); // Array ( [b] => brown [c] => blue [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的差集，用回调函数比较数据
**[array_udiff_assoc()]()**
```php
function value_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green",  "yellow", "red");
$result = array_udiff_assoc($array1, $array2, "value_compare_func");
print_r($result); // Array ( [b] => brown [c] => blue [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的差集，用回调函数比较数据和索引
**[array_udiff_uassoc()]()**
```php
function key_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

function value_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");

$result = array_udiff_uassoc($array1, $array2, "value_compare_func", "key_compare_func");
print_r($result); // Array ( [b] => brown [c] => blue [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 使用键名比较计算数组的差集
**[array_diff_key()]()**
```php
$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

$result = array_diff_key($array1, $array2);
print_r($result); // Array ( [red] => 2 [purple] => 4 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用回调函数对键名比较计算数组的差集
**[array_diff_ukey()]()**
```php
function key_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "red");

$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result); // Array ( [b] => brown [c] => blue [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

## 交集
### 计算数组的交集
**[array_intersect()]()**
```php
$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");

$result = array_intersect($array1, $array2);
print_r($result); // Array ( [a] => green [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 计算数组的交集，用回调函数比较数据
**[array_uintersect()]()**
```php
function value_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");

$result = array_uintersect($array1, $array2,'value_compare_func');
print_r($result); // Array ( [a] => green [0] => red )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的交集
**[array_intersect_assoc()]()**
```php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");

$result_array = array_intersect_assoc($array1, $array2);
print_r($result_array); // Array ( [a] => green )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的交集，用回调函数比较索引
**[array_intersect_uassoc()]()**
```php
function key_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");

$result_array = array_intersect_uassoc($array1, $array2,"key_compare_func");
print_r($result_array); // Array ( [a] => green )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 带索引检查计算数组的交集，用回调函数比较数据
**[array_uintersect_assoc()]()**
```php
function value_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");

$result_array = array_uintersect_assoc($array1, $array2, "value_compare_func");
print_r($result_array); // Array ( [a] => green )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


### 带索引检查计算数组的交集，用单独的回调函数比较数据和索引
**[array_uintersect_uassoc()]()**
```php
function key_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

function value_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b) ? 1 : -1;
}


$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");

$result_array = array_uintersect_uassoc($array1, $array2, "value_compare_func", "key_compare_func");
print_r($result_array); // Array ( [a] => green )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 使用键名比较计算数组的交集
**[array_intersect_key()]()**
```php
$array1 = array('blue' => 1, 'red' => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan' => 8);

$result = array_intersect_key($array1, $array2);
print_r($result); // Array ( [blue] => 1 [green] => 3 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)

### 用回调函数比较键名来计算数组的交集
**[array_intersect_ukey()]()**
```php

function key_compare_func($key1, $key2)
{
    if ($key1 === $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}
$array1 = array('blue' => 1, 'red' => 2, 'green' => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan' => 8);

$result = array_intersect_ukey($array1, $array2, "key_compare_func");
print_r($result); // Array ( [blue] => 1 [green] => 3 )
```
<br>[⬆ Back to top](#%E7%9B%AE%E5%BD%95)


