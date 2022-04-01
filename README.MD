Install:

```shell
pip install PhpBB-Utility
```

Example:

```python
from madyel import PhpBB

if __name__ == '__main__':
    config = {
        'ssh_host': '192.168.0.32',
        'ssh_username': 'root',
        'ssh_password': 'password',
        'ssh_port': 22,
        'database_username': 'phpBBUser',
        'database_password': 'phpBBPassword',
        'database_name': 'phpBBDB',
        'localhost': '127.0.0.1',
        'port_db': 3306,
    }
    p = PhpBB(config, enable_ssh=True)
    category_id_phpbb = 4
    username_phpbb = "lilli"
    title = "Hello"
    body_post = "Hello World"
    print(p.insert_topic_post(category_id_phpbb, username_phpbb, title, body_post))
    p.close()
```