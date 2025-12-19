# FlashErase 闪电擦除

普通的擦除工具写入量大，对固态硬盘（SSD）不友好，擦除机械硬盘（HDD）的文件速度慢；所以我编写了**闪电擦除**工具，**平衡擦除文件的安全与速度需求**。

![](FlashErase.gif)

## 特点

- **极速擦除**：快如闪电，大文件秒级擦除
- **低写入量**：减少固态硬盘耗损
- **批量处理**：支持多文件、文件夹递归、通配符处理，支持拖拽操作
- **超大文件支持**：最大支持16PB单文件

## 细节

- **擦除方式**：跳跃式擦除文件内容，每个文件擦除位置不一样；如果被擦除的文件本身是加密的（加密压缩包、加密镜像等等），是100%无法恢复的；如果文件本身不是加密的，会有碎片块（但是**足以抵御市面上所有的数据恢复软件**，即使实验室也**无法完整恢复**）。

## 使用方法

- 将文件/文件夹拖放至程序图标上，或通过命令行运行

### 命令行参数

```bash
# 处理单个文件
FlashErase file.pdf

# 处理多个文件
FlashErase photo.jpg data.csv

# 处理文件夹（会递归处理所有子文件）
FlashErase Documents

# 使用通配符
FlashErase *.txt
```

## 注意事项

- **它不是强删软件**，如果文件被其它软件占用，无法擦除
- 擦除前请确认文件无误，**一旦开始擦除，无法恢复**

## 相关项目

[想曰 - 文本加密让你想曰就曰](https://github.com/fzxx/XiangYue)

[文图变 - 文件藏到图片](https://github.com/fzxx/FileImgSwap)

[坏坏包 - 让压缩包像坏了](https://github.com/fzxx/NaughtyDamagePack)

## 下载地址

[https://github.com/fzxx/FlashErase/releases](https://github.com/fzxx/FlashErase/releases)