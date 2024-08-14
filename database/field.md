
# MySQL 中 不等于 会过滤掉 Null 的问题

## IFNULL()使用

* SELECT * FROM A WHERE IFNULL(B1,'')  != 1
