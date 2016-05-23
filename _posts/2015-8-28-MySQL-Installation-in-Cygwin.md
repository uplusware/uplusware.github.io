---
layout: post
title: MySQL Installation in Cygwin
---
1. To begin MySQL setup run the following:
	mysql_install_db

2. Run mysql - you'll get a firewall alert from windows if you have it active.
	mysqld_safe --user=xxxx&
 
3. Immediately following that, it would be wise to run the following:
	mysql_secure_installation
