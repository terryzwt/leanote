# 最新更新：
因为leanote现在收费了，目前该代码不继续维护。

### 说明
本镜像参考如下链接修改，但是进行了修正：

* [Run leanote by docker](https://github.com/leanote/leanote/wiki/Run-leanote-by-docker)
* [
EditNew Page
Leanote 二进制版详细安装教程 Mac and Linux](https://github.com/leanote/leanote/wiki/Leanote-%E4%BA%8C%E8%BF%9B%E5%88%B6%E7%89%88%E8%AF%A6%E7%BB%86%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B----Mac-and-Linux)

### 数据初始化
```bash
docker cp leanote_leanote-server_1:/usr/local/leanote/mongodb_backup/leanote_install_data init-data/
docker-compose exec leanote-db mongorestore -h localhost -d leanote --dir /tmp/init-data/leanote_install_data/
```
### demo用户
<pre>
user1 username: admin, password: abc123 (管理员, 只有该用户才有权管理后台, 请及时修改密码)
user2 username: demo@leanote.com, password: demo@leanote.com (仅供体验使用)
</pre>
