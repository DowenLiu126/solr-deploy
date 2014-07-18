solr-deploy
===========

方便solr插件开发的Maven化Solr Web环境。

此项目与Apache Solr官方提供的solr.war功能完全相同，只是使用Maven提供的jar进行了替换替换。  
使用Maven管理方便自开发插件的集成，尤其是方便了自开发插件的Debug。  
集成插件时在pom.xml文件中编写dependency即可，如集成我的[拼音扩展过滤器](https://github.com/DowenLiu126/pinyinTokenFilter)组件：  

	<dependency>
		<groupId>me.dowen.solr</groupId>
		<artifactId>pinyinTokenFilter</artifactId>
		<version>1.0.0-RELEASE</version>
		<scope>runtime</scope>
	</dependency>

此项目对原版Solr日志系统进行了替换，使用slf4j + logback的方式替换了原来的log4j。日志输出等级为INFO，具体设置及修改请自行查看logback项目说明
