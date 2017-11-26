# PlayFramework silhouette seed project with ScalikeJDBC

## MySQL

```bash
docker run --name example \
  -e MYSQL_ROOT_PASSWORD=password \
  -e MYSQL_DATABASE=example \
  -p 3306:3306 \
  -d mysql \
  --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci
```

```sql
CREATE TABLE USERS (
    id int AUTO_INCREMENT,
    user_id VARCHAR(300) NOT NULL UNIQUE,
    password VARCHAR(300) NOT NULL,
    first_name VARCHAR(300),
    last_name VARCHAR(300),
    email VARCHAR(300) not null,
    avatar_url VARCHAR(300),
    activated BOOLEAN DEFAULT FALSE,
    PRIMARY KEY (id),
    UNIQUE KEY pk_user_id (user_id)
);
```