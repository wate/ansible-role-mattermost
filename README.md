mattermost
=================

Setup Mattermost(work in progress)

OS Platform
-----------------

### Debian

- bullseye

Role Variables
--------------

設定方法の詳細については[defaults/main.yml](defaults/main.yml)のサンプルコードを参照してください。

### `mattermost_version`

Mattermostのバージョン

### `mattermost_listen_address_host`

### `mattermost_listen_address_port`

### `mattermost_db_cfg`

データベースの設定  
### Example  
#### PostgreSQL  
```yaml  
mattermost_db_cfg:  
type: postgres  
host: localhost  
port: 5432  
name: mattermost_test  
user: mmuser  
password: mostest  
encoding: utf8  
additional_params:  
- "sslmode=disable"  
- "connect_timeout=10"  
```  
#### MySQL  
```yaml  
mattermost_db_cfg:  
type: mysql  
host: localhost  
port: 3306  
name: mattermost_test  
user: mmuser  
password: mostest  
encoding: utf8mb4  
collation: utf8mb4_general_ci  
additional_params:  
- "charset=utf8mb4"  
- "writeTimeout=30s"  
```

### `mattermost_file_public_link_salt`

公開リンクのソルト設定

### `mattermost_sql_at_rest_encrypt_key`

SQLの暗号化設定

### `mattermost_service_gfycat_api_key`

gfycatのAPIキー  
詳細は以下のURLを参照  
https://developers.gfycat.com/api/

### `mattermost_service_gfycat_api_secret`

gfycatのAPIシークレット  
詳細は以下のURLを参照  
https://developers.gfycat.com/api/

### `mattermost_cfg`

Mattermostの設定

Example Playbook
--------------

```yaml
- hosts: servers
  roles:
    - role: mattermost
```

License
--------------

Apache License 2.0
