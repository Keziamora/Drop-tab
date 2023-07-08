# Drop-tab
Drop table after optimization
DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_lncel_fdd`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_lncel_fdd`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`) USING BTREE,KEY `3` (`mrbtsId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_lncel_fdd SELECT * FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5;

##### a_lte_mrbts_lnbts_lncel ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`) USING BTREE,KEY `3` (`mrbtsId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel SELECT * FROM a_lte_mrbts_lnbts_lncel_rc5;



##### a_lte_mrbts_lnbts_lncel_amlepr ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_amlepr`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_amlepr`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`amlePrId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`amlePrId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_amlepr_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_amlepr SELECT * FROM a_lte_mrbts_lnbts_lncel_amlepr_rc5;


##### a_lte_mrbts_lnbts_lncel_carel ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_carel`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_carel`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`caRelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`caRelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_carel_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_carel SELECT * FROM a_lte_mrbts_lnbts_lncel_carel_rc5;



##### a_lte_mrbts_lnbts_lncel_irfim ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_irfim`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_irfim`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`irfimId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`irfimId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_irfim_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_irfim SELECT * FROM a_lte_mrbts_lnbts_lncel_irfim_rc5;



##### a_lte_mrbts_lnbts_lncel_lnhoif ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_lnhoif`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_lnhoif`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`lnHoIfId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`lnHoIfId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_lnhoif_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_lnhoif SELECT * FROM a_lte_mrbts_lnbts_lncel_lnhoif_rc5;


##### a_lte_mrbts_lnbts_lncel_lnrel ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_lnrel`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_lnrel`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`lnRelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`lnRelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `3` (`mrbtsId`,`lnBtsId`,`lnCelId`,`ecgiAdjEnbId`,`ecgiLcrId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_lnrel_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_lnrel SELECT * FROM a_lte_mrbts_lnbts_lncel_lnrel_rc5;



##### a_lte_mrbts_lnbts_lncel_redrt ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_redrt`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_redrt`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`redrtId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`redrtId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_redrt_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_redrt SELECT * FROM a_lte_mrbts_lnbts_lncel_redrt_rc5;



##### a_lte_mrbts_lnbts_lncel_sib ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts_lncel_sib`;
CREATE TABLE `a_lte_mrbts_lnbts_lncel_sib`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`sibId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`sibId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_lncel_sib_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts_lncel_sib SELECT * FROM a_lte_mrbts_lnbts_lncel_sib_rc5;


##### a_lte_lncel_lc ####

DROP TABLE IF EXISTS `a_lte_lncel_lc`;
CREATE TABLE `a_lte_lncel_lc`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_lncel_lc_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_lncel_lc SELECT * FROM a_lte_lncel_lc_rc5;


##### a_lte_lncel_pc ####

DROP TABLE IF EXISTS `a_lte_lncel_pc`;
CREATE TABLE `a_lte_lncel_pc`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_lncel_pc_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_lncel_pc SELECT * FROM a_lte_lncel_pc_rc5;


##### a_lte_lncel_hc ####

DROP TABLE IF EXISTS `a_lte_lncel_hc`;
CREATE TABLE `a_lte_lncel_hc`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_lncel_hc_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_lncel_hc SELECT * FROM a_lte_lncel_hc_rc5;



##### a_lte_lncel_dc ####

DROP TABLE IF EXISTS `a_lte_lncel_dc`;
CREATE TABLE `a_lte_lncel_dc`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_lncel_dc_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_lncel_dc SELECT * FROM a_lte_lncel_dc_rc5;



##### a_lte_lncel_furtherplmnidl ####

DROP TABLE IF EXISTS `a_lte_lncel_furtherplmnidl`;
CREATE TABLE `a_lte_lncel_furtherplmnidl`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`,`lnCelId`,`listId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`,`lnCelId`,`listId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`,`lnCelId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_lncel_furtherplmnidl_smt WHERE CONCAT (mrbtsId,lnBtsId,lnCelId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId,lnCelId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId,a.lnCelId FROM a_lte_mrbts_lnbts_lncel_lncel_fdd_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_lncel_lncel_fdd_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId and a.lnCelId = b.lnCelId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid AND a.lnCelId = c.lncelid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_lncel_furtherplmnidl SELECT * FROM a_lte_lncel_furtherplmnidl_rc5;

##############################################################
########### MODIFY & INSERT LEVEL MRBTS LNBTS ################
##############################################################

##### a_lte_mrbts_lnbts ####

DROP TABLE IF EXISTS `a_lte_mrbts_lnbts`;
CREATE TABLE `a_lte_mrbts_lnbts`
  (PRIMARY KEY (`mrbtsId`,`lnBtsId`),UNIQUE KEY `1` (`mrbtsId`,`lnBtsId`) USING BTREE,KEY `2` (`mrbtsId`,`lnBtsId`) USING BTREE,KEY `3` (`mrbtsId`) USING BTREE)
	ENGINE = MyISAM DEFAULT CHARSET = utf8
SELECT * FROM a_lte_mrbts_lnbts_smt WHERE CONCAT (mrbtsId,lnBtsId) NOT IN 
	(SELECT
		DISTINCT(CONCAT(mrbtsId,lnBtsId))
	FROM
		(SELECT a.mrbtsId,a.lnBtsId FROM a_lte_mrbts_lnbts_rc5 a
			INNER JOIN a_lte_mrbts_lnbts_smt b ON a.mrbtsId = b.mrbtsId AND a.lnBtsId = b.lnBtsId
			LEFT JOIN 4g_list_mocn_ns c ON a.mrbtsId = c.mrbtsid AND a.lnBtsId = c.lnbtsid
			WHERE server_netact = 'H3I')a);
			
INSERT IGNORE INTO a_lte_mrbts_lnbts SELECT * FROM a_lte_mrbts_lnbts_rc5;
