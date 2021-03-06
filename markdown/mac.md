&nbsp;
#### 安装

下载: [百度云](https://pan.baidu.com/s/1M5geafwfc9sGUmLhG2SsLg) 或 [官方地址](https://download.docker.com/mac/stable/Docker.dmg)

![](http://img02.shangguantv.com/pic/install-mac-dmg.png)

&nbsp;
### 运行

从应用中找到 Docker 图标并点击运行。

![](http://img02.shangguantv.com/pic/install-mac-apps.png)

运行之后，会在右上角菜单栏看到多了一个鲸鱼图标，这个图标表明了 Docker 的运行状态。

![](http://img02.shangguantv.com/pic/install-mac-menu.png)

第一次点击图标，可能会看到这个安装成功的界面，点击 "Got it!" 可以关闭这个窗口。

![](http://img02.shangguantv.com/pic/install-mac-success.png)

以后每次点击鲸鱼图标会弹出操作菜单。

![](http://img02.shangguantv.com/pic/install-mac-menubar.png)

启动终端后，通过命令可以检查安装后的 Docker 版本。

```bash
$ docker --version
Docker version 19.03.1, build 74b1e89
$ docker-compose --version
docker-compose version 1.24.1, build 4667896b
$ docker-machine --version
docker-machine version 0.16.1, build cce350d7
```

### 下载加速

对于使用 macOS 的用户，在任务栏点击 Docker Desktop 应用图标 -> `Perferences`，在左侧导航菜单选择 `Docker Engine` (或者是：daemon)，在右侧像下边一样编辑 json 文件。修改完成之后，点击 `Apply & Restart` 按钮，Docker 就会重启并应用配置的镜像地址了。

```json
{
  "registry-mirrors": [
      "https://reg-mirror.qiniu.com",
      "https://dockerhub.azk8s.cn"
  ]
}
```

&nbsp;
### 检查加速器是否生效

执行 `$ docker info`，如果从结果中看到了如下内容，说明配置成功。

```bash
Registry Mirrors:
 https://reg-mirror.qiniu.com
```
