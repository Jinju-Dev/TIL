## [ mysql ]
#### Error: ER_NOT_SUPPORTED_AUTH_MODE: Client does not support authentication protocol requested by server; <br>
- mysql 설치 후 첫 연동 시 발생하는 에러
```sql
alter user 'root'@'localhost' identified with mysql_native_password by '1234'
```
