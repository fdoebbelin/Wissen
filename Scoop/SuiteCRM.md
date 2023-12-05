```bash
php ./bin/console suitecrm:app:install -u "admin" -p "admin" -U "root" -P "root" -H "localhost" -N "suitecrm" -S "localhost" -d "demo_data"
```


```sql
ALTER USER 'root'@'localhost' IDENTIFIED BY 'root';
CREATE DATABASE suitecrm;
```

Start Development Server

```
cd ./public
php -S localhost:8000
```
