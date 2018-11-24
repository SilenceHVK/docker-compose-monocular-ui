# docker-compose-monocular-ui
There are a lot of problems with installing Monocular UI with Helm. I found the Docker Compose installation method on the Internet and integrated it here.（使用 Helm 安装 Monocular UI 遇到了很多问题，在网上找到了 Docker Compose 安装的方法，在此整合一下）


## How to use

The following is an example of the CentOS 7 system. Docker is installed by default.

1. Clone project

```bash
$ git clone https://github.com/SilenceHVK/docker-compose-monocular-ui.git
```

2. Install python-pip

```bash
$ yum -y install epel-release
$ yum -y install python-pip
```

3. Upgrade pip

```bash
$ pip install --upgrade pip
```

4. Install Docker-Compose

```bash
$ pip install docker-compose
```
or
```bash
$ curl -L https://get.daocloud.io/docker/compose/releases/download/1.23.1/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose

$ chmod +x /usr/local/bin/docker-compose
```

5. Modify page port number
```bash
$ vi docker-compose-monocular-ui/docker-compose.yaml 
```

![修改页面端口号](https://github.com/SilenceHVK/docker-compose-monocular-ui/raw/master/docs/port-number.png)


6. Build project

```bash
$ docker-compose build
```

7. Run project

```bash
$ docker-compose up -d
```


![运行结果](https://github.com/SilenceHVK/docker-compose-monocular-ui/raw/master/docs/MonocularScreenshot.gif)
