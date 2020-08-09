# practiceProgress(부산IT교육센터 훈련진행 현황판)
부산IT교육센터 훈련진행과정을 관리하는 웹서비스를 의뢰받아 개발하였습니다. 

엑셀로 관리되던 훈련과정을 DB로 옮기고 실시간 훈련현황을 관리할 수 있습니다.
&nbsp;

## 기능
- 훈련과정 등록
- 훈련과정 수정
- 훈련과정 삭제
- 엑셀데이터 DB에 등록 및 훈련과정과 연계
- 엑셀데이터 검증
- 훈련과정 활성화 및 비활성화
- 당일 전체 훈련 확인

&nbsp;
&nbsp;
## 프레젠테이션
https://docs.google.com/presentation/d/1rVZnaeI76-AkdJjbl2RrEgBo3IDE1n5zZLjkih662og/edit?usp=sharing


&nbsp;
&nbsp;
## 영상
https://youtu.be/RfWTVgxJLhQ


&nbsp;
&nbsp;
## MySQL
### 스키마 생성

```sql
CREATE DATABASE `test_sch` /*!40100 DEFAULT CHARACTER SET utf8 */;
```


### db유저 아이디 비밀번호

```sql
-- 유저이름@아이피주소
create user 'bitc'@'%' identified by 'bitc5600';

-- ON DB이름.테이블명
-- TO 유저이름@아이피주소
GRANT ALL PRIVILEGES ON *.* TO 'bitc'@'%';
ALTER DATABASE test_sch CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
use test_sch;
```



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

