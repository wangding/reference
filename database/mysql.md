# MySQL

## 修改数据库密码强度（v5.7）

- SHOW VARIABLES LIKE 'validate_password%';
- set global validate_password_policy=0;
- set global validate_password_length=3;

