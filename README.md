# Prototype-based-LLM-assisted-LCCE-assessment
For the residential building's LCCE assessment
# 基于典型建筑库的全生命周期碳排放评估系统

<p align="center">
  <img src="images/logo.png" alt="logo" width="160">
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/你的用户名/你的仓库名?style=flat-square" alt="release">
  <img src="https://img.shields.io/github/downloads/你的用户名/你的仓库名/total?style=flat-square" alt="downloads">
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

## 项目简介

本系统基于典型建筑原型库，结合大语言模型解析与建筑能耗模拟，实现从建筑描述输入到碳排放结果输出的自动化计算流程。

用户可通过自然语言描述或 Excel 参数表输入建筑信息。系统会自动匹配原型模型，完成参数修改与 EnergyPlus 模拟，并输出建筑能耗、运行碳排放、隐含碳排放和全生命周期碳排放结果。

该软件主要面向以下用户：

- 建筑设计人员
- 建筑节能与低碳研究人员
- 建筑模拟与性能评估人员
- 教学与科研场景中的学生和教师

---

## News

- **[最新版本]** 发布桌面版 GUI 程序，支持单体模拟、批量模拟、结果查看和配置管理。
- **[更新]** 新增自然语言输入模式，支持通过 DeepSeek API 自动解析建筑参数。
- **[更新]** 新增批量计算功能，支持 Excel 批量和自然语言批量两种模式。
- **[更新]** 新增授权激活机制与加密模板保护机制。


---

## Key Features

- **自然语言输入**  
  支持直接输入建筑描述，自动提取关键建模参数。

- **原型模型匹配**  
  基于典型建筑库自动匹配最接近的原型模型。

- **自动能耗模拟**  
  自动调用 EnergyPlus 完成建筑能耗模拟。

- **全生命周期碳评估**  
  支持运行碳排放、隐含碳排放和全生命周期碳排放计算。

- **单体与批量模式**  
  支持单个方案快速评估，也支持多方案批量对比。

- **图形界面操作**  
  提供桌面 GUI，无需命令行基础即可上手使用。

---

## 软件界面

### 首页
![首页](images/home.png)

### 单体模拟
![单体模拟](images/single_sim.png)

### 批量模拟
![批量模拟](images/batch_sim.png)

### 结果查看
![结果查看](images/results.png)



---

## 功能概览

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

## Workflow

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
