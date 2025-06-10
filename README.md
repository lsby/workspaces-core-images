# Kasm 核心镜像 (改)

## 分支

分支自: https://github.com/kasmtech/workspaces-core-images

## 设置用户名密码

原镜像不允许设置用户名, 我修改了这一点.

还有一个纯查看账号, 改为了`${VNC_NAME}_viewer`,
例如, 如果 `VNC_NAME` 是 `admin`, 那么该账号就是`admin_viewer`,
但好像不能用.

使用方法:

```
docker run --rm -it --shm-size=512m -p 6901:6901 -e VNC_NAME admin -e VNC_PW 123456 -e VNC_VIEW_ONLY_PW 123456 kasm-core
```
