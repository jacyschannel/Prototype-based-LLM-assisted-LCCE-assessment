# Prototype-based-LLM-assisted-LCCE-assessment
For the residential building's LCCE assessment
# 🏠 基于典型建筑库的全生命周期碳排放评估系统

<p align="center">
  <img src="images/logo.png" alt="logo" width="160">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11-blue?style=flat-square" alt="platform">
  <img src="https://img.shields.io/badge/EnergyPlus-9.4%2B-success?style=flat-square" alt="energyplus">
  <img src="https://img.shields.io/badge/license-Commercial%20or%20Custom-orange?style=flat-square" alt="license">
</p>

<p align="center">
  中文版 | <a href="README_EN.md">English</a>
</p>

<p align="center">
  一个面向住宅建筑的桌面软件，支持自然语言输入、原型模型匹配、EnergyPlus 自动模拟，以及运行碳排放、隐含碳排放和全生命周期碳排放评估。
</p>

---

## 📌 项目简介

本系统基于典型建筑原型库，结合大语言模型解析与建筑能耗模拟，实现从建筑描述输入到碳排放结果输出的自动化计算流程。

用户可通过自然语言描述或 Excel 参数表输入建筑信息。系统会自动匹配原型模型，完成参数修改与 EnergyPlus 模拟，并输出建筑能耗、运行碳排放、隐含碳排放和全生命周期碳排放结果。

该软件主要面向以下用户：

- 建筑设计人员
- 建筑节能与低碳研究人员
- 建筑模拟与性能评估人员
- 教学与科研场景中的学生和教师

---

## 📰 News

- **[最新版本]** 发布桌面版 GUI 程序，支持单体模拟、批量模拟、结果查看和配置管理。
- **[更新]** 新增自然语言输入模式，支持通过 DeepSeek API 自动解析建筑参数。
- **[更新]** 新增批量计算功能，支持 Excel 批量和自然语言批量两种模式。
- **[更新]** 新增授权激活机制与加密模板保护机制。

---

## ✨ Key Features

- **📝 自然语言输入**  
  支持直接输入建筑描述，自动提取关键建模参数。

- **🏢 原型模型匹配**  
  基于典型建筑库自动匹配最接近的原型模型。

- **⚙️ 自动能耗模拟**  
  自动调用 EnergyPlus 完成建筑能耗模拟。

- **🌱 全生命周期碳评估**  
  支持运行碳排放、隐含碳排放和全生命周期碳排放计算。

- **📊 单体与批量模式**  
  支持单个方案快速评估，也支持多方案批量对比。

- **🖥️ 图形界面操作**  
  提供桌面 GUI，无需命令行基础即可上手使用。

---

## 🖼️ 软件界面

### 首页
![首页](images/home.png)

### 单体模拟
![单体模拟](images/single_sim.png)

### 批量模拟
![批量模拟](images/batch_sim.png)

### 结果查看
![结果查看](images/results.png)

---

## 🔍 功能概览

### 1. 单体模拟
适用于单个建筑方案的快速评估。

支持：
- 自然语言输入
- 手动参数输入
- 自定义气象文件
- 自定义电网碳因子
- 运行结果查看与导出

### 2. 批量模拟
适用于多个建筑方案的集中评估与对比。

支持：
- Excel 批量输入
- 多条自然语言批量输入
- 自动生成案例结果文件夹
- 自动汇总批量结果表

### 3. 结果查看
支持：
- 浏览历史模拟结果
- 查看详细表格
- 导出 CSV / Excel 文件

### 4. 配置管理
支持：
- DeepSeek API 配置
- EnergyPlus 路径配置
- 默认气象文件配置
- 本地参数保存

---

## 🔄 Workflow

本软件的主要流程如下：

```text
用户输入
   ↓
自然语言解析 / 参数读取
   ↓
原型模型匹配
   ↓
模型参数自动修改
   ↓
EnergyPlus 模拟
   ↓
结果提取
   ↓
运行碳排放计算
   ↓
隐含碳排放计算
   ↓
全生命周期碳排放汇总输出
```

---

## 🚀 Quick Start

### 1. 下载软件

请前往本仓库的 **Releases** 页面下载最新版本压缩包。

下载并解压后，目录通常类似于：

```text
CarbonCalc/
├── CarbonCalc.exe
├── 板式/
├── *.epw
├── *.xlsx
├── _internal/
└── 其他必要文件
```

### 2. 安装 EnergyPlus

本软件依赖 EnergyPlus 进行能耗模拟，请先安装：

- **EnergyPlus 9.4.0 **

安装完成后，请确认以下文件存在：

- `energyplus.exe`
- `Energy+.idd`

### 3. 首次启动

双击运行：

```text
CarbonCalc.exe
```

首次启动时，请依次完成以下配置：

#### 步骤一：导入 License
1. 启动软件
2. 记录机器码
3. 将机器码发送给管理员
4. 获取 `license.key`
5. 点击“导入 License 文件”
6. 导入成功后进入主界面
p.s. 目前我们为完全开放，不需要导入License即可使用哦

#### 步骤二：配置 DeepSeek API
进入“配置管理”页面，填写：
- API Key
- API Base URL
这里可以访问DeepSeek官网进行API充值，0.1元可用100次左右

然后点击：
- 测试连接
- 保存配置

#### 步骤三：配置 EnergyPlus 路径
进入“配置管理”页面，设置：
- `energyplus.exe` 路径
- `Energy+.idd` 路径
- 默认气象文件路径

完成后即可开始模拟。

---

## 📘 使用说明

### 单体模拟

1. 进入“单体模拟”页面  
2. 选择输入方式  
   - 自然语言描述  
   - 手动参数输入  
3. 设置气象文件与电网碳因子  
4. 点击“开始模拟”  
5. 查看结果  

输出内容通常包括：
- 建筑能耗结果
- 运行碳排放结果
- 隐含碳排放结果
- 全生命周期碳排放结果
- 材料清单

### 批量模拟

1. 进入“批量模拟”页面  
2. 选择模式  
   - Excel 批量  
   - 自然语言批量  
3. 选择输入文件或输入多条描述  
4. 设置输出目录  
5. 点击“开始批量计算”  
6. 查看汇总结果  

---

## 💬 自然语言输入示例

```text
6层板式住宅，朝向为南北向，外墙传热系数为0.15 W/(m²·K)，窗户K值为1.2 W/(m²·K)，太阳能得热系数为0.3，可见光透射率为0.8。南北向窗墙比为0.4，东西向窗墙比为0.1，照明功率密度2.5，设备功率密度10.0。
```

系统通常可识别以下信息：

- 建筑类型
- 层数
- 朝向
- 外墙热工参数
- 窗户热工参数
- 各朝向窗墙比
- 照明功率密度
- 设备功率密度

---

## 📂 输出结果

软件输出通常包括：

- 修改后的模型文件
- EnergyPlus 模拟结果文件
- 建筑分项能耗结果
- 运行碳排放结果
- 隐含碳排放结果
- 全生命周期碳排放结果
- 批量汇总表

---

## 💻 系统要求

- 操作系统：Windows 10 / 11（64 位）
- EnergyPlus：9.4.0 或更高版本
- 磁盘空间：建议至少 2 GB
- 网络：使用自然语言智能解析时需要联网

---

## ❓ 常见问题

### 1. 软件无法启动
请检查：
- 是否完整解压压缩包
- 是否误删 `_internal` 或其他附属文件


### 2. 模拟失败
请检查：
- `energyplus.exe` 路径是否正确
- `Energy+.idd` 路径是否正确
- 气象文件是否存在
- 输出目录中的 `eplusout.err` 是否有报错信息

### 3. 自然语言解析失败
请检查：
- DeepSeek API Key 是否填写正确
- 网络是否正常
- API 服务是否可用


---

## 📝 更新日志

### v1.0.0
- 发布首个桌面版 GUI 程序
- 支持单体模拟
- 支持批量模拟
- 支持自然语言输入
- 支持全生命周期碳排放评估



---

## 📮 联系方式

如需授权、合作或技术支持，请联系项目维护者。

- 官网：[buildingdata.xauat.edu.cn](https://buildingdata.xauat.edu.cn/)
- Issues：欢迎通过 GitHub Issues 提交问题
- Email：jiangshuxin@xauat.edu.cn

---

## ⭐ 助力！

如果这个项目对你有帮助，欢迎点一个 Star。
当然，也欢迎您引用本人文章~

