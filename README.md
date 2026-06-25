# Golang 中文学习文档

本项目 fork 自: [Open Source CQUT/Golang-Doc](https://github.com/Open-Source-CQUT/Golang-Doc) ，感谢原项目的成果，本人在其基础上增加了部分自己在学习过程中认为需要注意的知识点。

## 开发

文档本身采用 [VuePress](https://vuejs.press/zh/) 框架和 [VuePress Theme Hope](https://theme-hope.vuejs.press/zh/) 主题进行开发，上手难度低，使用简单，并采用 `pnpm` 进行构建。

**准备**

在进行开发之前，请确保本地的 nodejs 版本是 18.19 及以上：

```bash
$ node -v
v22.12.0
```

之后请启用 Corepack (Windows 系统需要管理员权限)：

```bash
corepack enable
```

如遇到框架相关的问题请自行浏览官方网站。

**安装依赖**

```bash
pnpm install
```

**本地运行**

```bash
pnpm docs:dev
```

**清空缓存运行**

```bash
pnpm docs:clean-dev
```

**构建**

```bash
pnpm docs:build
```
