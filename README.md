# chuntiangarten
纯粹属于个人练手，为幼儿园做的jsp小项目，JSP+MySQL，并试着部署到了百度BAE


以下是从MySQL导出来的数据库文件，新建个xxx.sql文件复制进去就行。


-- MySQL Administrator dump 1.4
--
-- ------------------------------------------------------
-- Server version	5.0.45-community-nt


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;

/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;


--
-- Create schema test
--

CREATE DATABASE IF NOT EXISTS test;
USE test;

--
-- Definition of table `food`
--

DROP TABLE IF EXISTS `food`;
CREATE TABLE `food` (
  `id` int(10) unsigned NOT NULL auto_increment,
  `date` int(10) unsigned NOT NULL,
  `class` varchar(45) NOT NULL,
  `m1` varchar(45) NOT NULL COMMENT '第一餐',
  `m2` varchar(45) NOT NULL,
  `m3` varchar(45) NOT NULL,
  `m4` varchar(45) NOT NULL,
  `m5` varchar(45) NOT NULL,
  PRIMARY KEY  (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=45 DEFAULT CHARSET=latin1 COMMENT='伙食';

--
-- Dumping data for table `food`
--

/*!40000 ALTER TABLE `food` DISABLE KEYS */;
INSERT INTO `food` (`id`,`date`,`class`,`m1`,`m2`,`m3`,`m4`,`m5`) VALUES 
 (3,123,'w','w','w','w','w','e'),
 (44,22222,'22222','2222222222','2222222222','222222222222','22','22');
/*!40000 ALTER TABLE `food` ENABLE KEYS */;


--
-- Definition of table `kidfee`
--

DROP TABLE IF EXISTS `kidfee`;
CREATE TABLE `kidfee` (
  `xh` int(10) unsigned NOT NULL auto_increment COMMENT '宝宝号码',
  `name` varchar(45) NOT NULL,
  `class` varchar(45) NOT NULL,
  `month` varchar(45) NOT NULL COMMENT '欠费月份',
  `foodFee` int(10) unsigned NOT NULL,
  `kidfee` int(10) unsigned NOT NULL COMMENT '已交费用',
  `payed` int(10) unsigned NOT NULL,
  PRIMARY KEY  (`xh`)
) ENGINE=InnoDB AUTO_INCREMENT=22223 DEFAULT CHARSET=latin1 COMMENT='托费查询';

--
-- Dumping data for table `kidfee`
--

/*!40000 ALTER TABLE `kidfee` DISABLE KEYS */;
INSERT INTO `kidfee` (`xh`,`name`,`class`,`month`,`foodFee`,`kidfee`,`payed`) VALUES 
 (103,'bob2','tuo2','1412',200,180,21),
 (22222,'1','1','1',1,1,1);
/*!40000 ALTER TABLE `kidfee` ENABLE KEYS */;


--
-- Definition of table `leaverecord`
--

DROP TABLE IF EXISTS `leaverecord`;
CREATE TABLE `leaverecord` (
  `id` int(10) unsigned NOT NULL auto_increment,
  `Bh` varchar(45) NOT NULL,
  `Date` varchar(45) NOT NULL,
  `Reason` varchar(45) NOT NULL,
  PRIMARY KEY  (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `leaverecord`
--

/*!40000 ALTER TABLE `leaverecord` DISABLE KEYS */;
/*!40000 ALTER TABLE `leaverecord` ENABLE KEYS */;


--
-- Definition of table `suggestion`
--

DROP TABLE IF EXISTS `suggestion`;
CREATE TABLE `suggestion` (
  `id` int(11) NOT NULL,
  `suggestion` varchar(45) NOT NULL,
  `date` varchar(45) NOT NULL,
  PRIMARY KEY  (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `suggestion`
--

/*!40000 ALTER TABLE `suggestion` DISABLE KEYS */;
/*!40000 ALTER TABLE `suggestion` ENABLE KEYS */;




/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
