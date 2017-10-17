运行命令

`docker volume create --name gitlab-data -d local`

创建一个本地的数据卷

执行命令
start.bat

##### 汉化
1. 将汉化文件copy到 config下
2. 命令 `docker exec -it zrdgitlab /bin/bash` 进入容器
3. 命令 `apt-get update` 更新软件源
4. 命令 `apt-get install patch` 安装patch
5. 命令 `cd /etc/gitlab` 切换到gitlab目录下
6. 命令 `patch -d /opt/gitlab/embedded/service/gitlab-rails -p1 < v10.0.1.*.diff` 解压资源文件
7. 命令 `gitlab-ctl reconfigure`重新配置gitlab
8. 命令 `gitlab-ctl restart`重启gitlab