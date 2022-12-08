mattermost
=================

Setup Mattermost

OS Platform
-----------------

### Debian

- bullseye

Role Variables
--------------

### `mattermost_version`

Mattermostのバージョン

### `mattermost_listen_address_host`

### `mattermost_listen_address_port`

### `mattermost_db_cfg`

データベースの設定

### `mattermost_smtp_cfg`

SMTPの設定

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
