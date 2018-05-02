# YafDock
Docker 下的 Yaf 开发环境.

## 支持的软件（镜像）

- **数据库**
    - MySQL
- **数据库管理**
    - PhpMyAdmin
- **缓存引擎:**
    - Redis
    - Memcached
- **WEB 服务器**
    - Nginx
- **PHP**
    - php-fpm
- **工具:**
    - Workspace (PHP-CLI, xDebug, Composer, Git, Node, Yarn, Gulp, Vim, cURL...)

## 安装

1. 在你的 Yaf 项目中克隆 `yafdock` :
```bash
git clone https://github.com/jochen/yafdock.git
```

2. 进入 `yafdock` 文件夹并将 `.env-example` 复制为 `.env`
```bash
cd yafdock
cp .env.example .env
```

> 查看 .env 文件你会发现很多服务配置项，在这里可以自行配置自己的开发环境。

3. 运行容器：
```bash
docker-compose up -d
```

4. 打开你的项目配置文件并设置服务配置信息，例如：
```bash
DB_HOST=mysql
REDIS_HOST=redis
MEMCACHE_HOST=memcached
```

> 将配置文件中的各种服务的 `host` 改为相应的容器名称
