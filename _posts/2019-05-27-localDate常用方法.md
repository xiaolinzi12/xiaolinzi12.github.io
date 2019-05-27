---
layout: post
title:  "LocalDate常用方法总结"
date: 2019-05-27 19:50:17 +0800
categories: Java LocalDate
---
## LocalDate常用方法总结
### 1. 简介
	* LocalDate 只包含了年月日的信息，不包含时间和时区。
	* LocalDate 重写了 toString() 方法，一般的格式为 "yyyy-MM-dd"
### 2. 常用方法
	* 加法 LocalDate.now().plusDays(1)
	* 减法 LocalDate.now().minusDays(1)
	
#### Date to LocalDate
	
````
   * Date date = new Date();
   // atZone()方法返回在指定时区从此Instant生成的ZonedDateTime。
   * LocalDate localDate = date.toInstant().atZone(ZoneId.systemDefault()).toLocalDate();    
````
#### LocalDate to Date
		
````
   * Date date = Date.form(LocalDate.now().atStartOfDay(ZoneId.systemDefault()))    
```` 
#### LocalTime to String - 其它类似

````
	LocalTime.now().format(DateTimeFormatter.ofPattern("HHmmss"))
````