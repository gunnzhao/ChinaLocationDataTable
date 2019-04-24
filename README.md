# 中国省市区详细数据表

直接将locations.sql导入到MySQL中即可使用

## 表名称 locations

## 表字段描述

字段 | 类型 | 描述
----|------|----
id | int(7) | 主键
name | varchar(40) | 省市区名称
parentid | int(7) | 上级ID
shortname | varchar(40) | 简称
leveltype | tinyint(2) | 级别:0,中国；1，省分；2，市；3，区、县
citycode | varchar(7) | 城市代码
zipcode | varchar(7) | 邮编
lng | varchar(20) | 经度
lat | varchar(20) | 纬度
pinyin | varchar(40) | 拼音
status | enum('0','1') | 状态

## 表结构

```sql
CREATE TABLE `locations` (
  `id` int(7) NOT NULL COMMENT '主键',
  `name` varchar(40) DEFAULT NULL COMMENT '省市区名称',
  `parentid` int(7) DEFAULT NULL COMMENT '上级ID',
  `shortname` varchar(40) DEFAULT NULL COMMENT '简称',
  `leveltype` tinyint(2) DEFAULT NULL COMMENT '级别:0,中国；1，省分；2，市；3，区、县',
  `citycode` varchar(7) DEFAULT NULL COMMENT '城市代码',
  `zipcode` varchar(7) DEFAULT NULL COMMENT '邮编',
  `lng` varchar(20) DEFAULT NULL COMMENT '经度',
  `lat` varchar(20) DEFAULT NULL COMMENT '纬度',
  `pinyin` varchar(40) DEFAULT NULL COMMENT '拼音',
  `status` enum('0','1') DEFAULT '1'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```
