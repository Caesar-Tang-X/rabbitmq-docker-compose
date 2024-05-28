# RabbitMQ Docker Compose YML File


## 简介
    docker 一键启动 rabbitmq 容器的 docker-compose.yml 配置


## 镜像环境：
	rabbitmq:3.10-management-alpine


## 启动命令：
	docker-compose up -d


##  安装及生成数据路径：
    ├── rabbitmq 
        ├── conf                        配置文件目录
            ├── 10-defaults.conf            10-defaults 配置文件
            └── rabbitmq.conf               rabbitmq 配置文件
        ├── data                        数据目录
        ├── log                         日志目录
        ├── docker-compose.yml          docker-compose.yml
        └── README.md                   README.md


## 隐私信息配置：
	1. 修改 RabbitMQ 初始用户密码, 文件路径：docker-compose.yml


## 安装延时插件：
	1. 进入插件官网：
        插件官网：https://www.rabbitmq.com/community-plugins.html
        延时插件下载地址：https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/3.10.0/rabbitmq_delayed_message_exchange-3.10.0.ez
    2. 下载插件（和rabbitmq版本保持一致，不然可能会报错无法安装）
    3. 将插件压缩包放入容器内的插件目录：
        /opt/rabbitmq/plugins/
    4. 安装插件：
        rabbitmq-plugins enable rabbitmq_delayed_message_exchange
    5. 查看插件列表：
        rabbitmq-plugins list 

