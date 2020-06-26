# practiceProgress



## MySQL



### class_table
```sql
CREATE TABLE `class_table` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `room` int(11) DEFAULT NULL,
  `class_name` varchar(300) DEFAULT NULL,
  `class_part` varchar(10) DEFAULT NULL,
  `class_open` date DEFAULT NULL,
  `class_close` date DEFAULT NULL,
  `homeroom_prof` varchar(20) DEFAULT NULL,
  `excel_name` varchar(300) DEFAULT NULL,
  `status` varchar(8) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```



### practice_table

```sql
CREATE TABLE `practice_table` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `class_name` varchar(300) DEFAULT NULL,
  `class_date` date DEFAULT NULL,
  `day_week` varchar(4) DEFAULT NULL,
  `class_time` int(11) DEFAULT NULL,
  `start_time` varchar(11) DEFAULT NULL,
  `end_time` varchar(11) DEFAULT NULL,
  `subject1` varchar(100) DEFAULT NULL,
  `subject2` varchar(100) DEFAULT NULL,
  `prof` varchar(20) DEFAULT NULL,
  `room` int(11) DEFAULT NULL,
  `class_id` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```

