# Phicomm N1 OpenWrt 自动编译

本项目使用 GitHub Actions 自动编译 OpenWrt 官方源码，并使用 [unifreq/openwrt_packit](https://github.com/unifreq/openwrt_packit) 打包成 Phicomm N1 可用的固件。

## 使用方法

1. Fork 本仓库到你的 GitHub 账号。
2. 进入仓库的 **Actions** 页面，启用 Workflows。
3. 点击 **Build OpenWrt for Phicomm N1**，然后点击 **Run workflow**。
4. 编译完成后，固件会自动上传到本仓库的 **Releases** 页面。

## 默认信息

- 默认 IP：`192.168.1.1`
- 默认账号：`root`
- 默认密码：`password`

## 自定义

- 修改 `.github/workflows/build-n1-openwrt.yml` 中的 `OPENWRT_BRANCH` 可切换 OpenWrt 版本。
- 在 `Configure OpenWrt` 步骤中增删 `CONFIG_PACKAGE_*` 可定制软件包。
- 修改 `KERNEL_VERSION_NAME` 可指定内核系列（需与源码内核匹配）。

## 致谢

- [OpenWrt](https://github.com/openwrt/openwrt)
- [unifreq/openwrt_packit](https://github.com/unifreq/openwrt_packit)
- [ophub](https://github.com/ophub)
