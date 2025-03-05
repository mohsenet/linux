## Redis

### Install redis and check size of appendonly.aof 
```bash
sudo apt install redis-server
sudo vi /etc/redis/redis.conf
    bind 127.0.0.1
    requirepass YOUR_PASSWORD
    appendonly yes
    appendfilename "appendonly.aof"
# sudo systemctl enable redis-server.service
sudo systemctl restart redis-server.service
redis-cli INFO server
# for check size of [appendonly.aof, dump.rdb]:
sudo ls /var/lib/redis/
sudo du -h /var/lib/redis/appendonly.aof
sudo du -h /var/lib/redis/dump.rdb
```
