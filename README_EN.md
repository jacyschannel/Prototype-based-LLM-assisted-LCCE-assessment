# Prototype-based-LLM-assisted-LCCE-assessment
For residential building life-cycle carbon emissions assessment

# 🏠 Whole Life-Cycle Carbon Emission Assessment System Based on a Typical Building Library

<p align="center">
  <img src="images/logo.png" alt="logo" width="160">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows%2010%2F11-blue?style=flat-square" alt="platform">
  <img src="https://img.shields.io/badge/EnergyPlus-9.4%2B-success?style=flat-square" alt="energyplus">
  <img src="https://img.shields.io/badge/license-Commercial%20or%20Custom-orange?style=flat-square" alt="license">
</p>

<p align="center">
  <a href="README.md">中文</a> | English
</p>

<p align="center">
  A desktop application for residential buildings that supports natural-language input, prototype model matching, automated EnergyPlus simulation, and the assessment of operational carbon, embodied carbon, and life-cycle carbon emissions.
</p>

---

## 📌 Overview

This system is built on a library of typical building prototypes and combines large language model parsing with building energy simulation to automate the workflow from building description input to carbon assessment output.

Users can input building information through natural-language descriptions or Excel parameter tables. The system automatically matches a prototype model, modifies the relevant parameters, runs EnergyPlus simulations, and outputs building energy use, operational carbon emissions, embodied carbon emissions, and life-cycle carbon emissions.

This software is mainly intended for:

- building designers
- researchers in building energy efficiency and low-carbon design
- users involved in building simulation and performance assessment
- students and teachers in teaching and research scenarios

---

## 📰 News

- **[Latest]** Released the desktop GUI version, supporting single-case simulation, batch simulation, result viewing, and configuration management.
- **[Update]** Added a natural-language input mode, supporting automatic parsing of building parameters through the DeepSeek API.
- **[Update]** Added batch calculation functions, supporting both Excel-based batch input and natural-language batch input.
- **[Update]** Added an activation mechanism and encrypted template protection.

---

## ✨ Key Features

- **📝 Natural-language input**  
  Supports direct building descriptions and automatically extracts key modeling parameters.

- **🏢 Prototype model matching**  
  Automatically matches the closest prototype model based on a typical building library.

- **⚙️ Automated energy simulation**  
  Automatically calls EnergyPlus to perform building energy simulations.

- **🌱 Life-cycle carbon assessment**  
  Supports the calculation of operational carbon emissions, embodied carbon emissions, and life-cycle carbon emissions.

- **📊 Single-case and batch modes**  
  Supports both rapid evaluation of a single scheme and batch comparison of multiple schemes.

- **🖥️ Graphical user interface**  
  Provides a desktop GUI, allowing users to get started without command-line experience.

---

## 🖼️ Interface Preview

### Home
![Home](images/home.png)

### Single Simulation
![Single Simulation](images/single_sim.png)

### Batch Simulation
![Batch Simulation](images/batch_sim.png)

### Results Viewer
![Results Viewer](images/results.png)

---

## 🔍 Function Overview

### 1. Single Simulation
Designed for rapid assessment of a single building scheme.

Supported functions:
- natural-language input
- manual parameter input
- custom weather files
- custom electricity carbon factors
- result viewing and export

### 2. Batch Simulation
Designed for centralized evaluation and comparison of multiple building schemes.

Supported functions:
- Excel batch input
- multiple natural-language inputs
- automatic generation of case result folders
- automatic generation of batch summary tables

### 3. Results Viewer
Supports:
- browsing historical simulation results
- viewing detailed tables
- exporting CSV / Excel files

### 4. Configuration Management
Supports:
- DeepSeek API configuration
- EnergyPlus path configuration
- default weather file configuration
- local parameter storage

---

## 🔄 Workflow

The main workflow of the software is as follows:

```text
User Input
   ↓
Natural-Language Parsing / Parameter Reading
   ↓
Prototype Model Matching
   ↓
Automatic Model Parameter Modification
   ↓
EnergyPlus Simulation
   ↓
Result Extraction
   ↓
Operational Carbon Calculation
   ↓
Embodied Carbon Calculation
   ↓
Life-Cycle Carbon Emissions Output
```

---

## 🚀 Quick Start

### 1. Download the Software

Please go to the **Releases** page of this repository to download the latest version package.

After downloading and extracting it, the directory typically looks like this:

```text
CarbonCalc/
├── CarbonCalc.exe
├── 板式/
├── *.epw
├── *.xlsx
├── _internal/
└── other required files
```

### 2. Install EnergyPlus

This software depends on EnergyPlus for energy simulation. Please install:

- **EnergyPlus 9.4.0**

After installation, please make sure the following files are available:

- `energyplus.exe`
- `Energy+.idd`

### 3. First Launch

Double-click to run:

```text
CarbonCalc.exe
```

When launching for the first time, please complete the following configuration steps:

#### Step 1: Import License
1. Launch the software
2. Record the machine code
3. Send the machine code to the administrator
4. Obtain the `license.key`
5. Click “Import License File”
6. Enter the main interface after successful import

🤭 At present, the software is fully open, so you can use it directly without importing a License.

#### Step 2: Configure the DeepSeek API
Go to the “Configuration Management” page and fill in:
- API Key
- API Base URL

You can visit the DeepSeek official website to top up your API balance. As a rough estimate, RMB 0.1 is enough for about 100 uses.

Then click:
- Test Connection
- Save Configuration

#### Step 3: Configure the EnergyPlus Path
Go to the “Configuration Management” page and set:
- the path to `energyplus.exe`
- the path to `Energy+.idd`
- the default weather file path

After that, you can start the simulation.

---

## 📘 User Guide

### Single Simulation

1. Go to the “Single Simulation” page  
2. Choose the input method  
   - natural-language description  
   - manual parameter input  
3. Set the weather file and electricity carbon factor  
4. Click “Start Simulation”  
5. View the results  

Typical outputs include:
- building energy results
- operational carbon emissions results
- embodied carbon emissions results
- life-cycle carbon emissions results
- material list

### Batch Simulation

1. Go to the “Batch Simulation” page  
2. Select the mode  
   - Excel batch  
   - natural-language batch  
3. Select the input file or enter multiple descriptions  
4. Set the output directory  
5. Click “Start Batch Calculation”  
6. View the summary results  

---

## 💬 Natural-Language Input Example

```text
A 6-story slab-type residential building with a north-south orientation, an exterior wall U-value of 0.15 W/(m²·K), a window U-value of 1.2 W/(m²·K), a solar heat gain coefficient of 0.3, and a visible transmittance of 0.8. The north and south window-to-wall ratios are 0.4, and the east and west window-to-wall ratios are 0.1. The lighting power density is 2.5, and the equipment power density is 10.0.
```

The system can usually recognize the following information:

- building type
- number of stories
- orientation
- exterior wall thermal properties
- window thermal properties
- window-to-wall ratios by orientation
- lighting power density
- equipment power density

---

## 📂 Output Results

Typical outputs of the software include:

- modified model files
- EnergyPlus simulation output files
- end-use energy results
- operational carbon emissions results
- embodied carbon emissions results
- life-cycle carbon emissions results
- batch summary tables

---

## 💻 System Requirements

- Operating System: Windows 10 / 11 (64-bit)
- EnergyPlus: 9.4.0 or higher
- Disk Space: at least 2 GB recommended
- Network: required when using the natural-language intelligent parsing function

---

## ❓ FAQ

### 1. The software cannot start
Please check:
- whether the compressed package has been fully extracted
- whether `_internal` or other attached files have been accidentally deleted

### 2. Simulation failed
Please check:
- whether the `energyplus.exe` path is correct
- whether the `Energy+.idd` path is correct
- whether the weather file exists
- whether there is any error information in `eplusout.err` under the output directory

### 3. Natural-language parsing failed
Please check:
- whether the DeepSeek API Key is correct
- whether the network connection is normal
- whether the API service is available

---

## 📝 Changelog

### v1.0.0
- Released the first desktop GUI version
- Supports single-case simulation
- Supports batch simulation
- Supports natural-language input
- Supports life-cycle carbon emissions assessment

---

## 📮 Contact

For authorization, collaboration, or technical support, please contact the project maintainer.

- Official website: [buildingdata.xauat.edu.cn](https://buildingdata.xauat.edu.cn/)
- Issues: welcome to submit questions through GitHub Issues
- Email: jiangshuxin@xauat.edu.cn

---

## ⭐ Support Us!

If this project is helpful to you, please consider giving it a Star.  
You are also welcome to cite the author's related papers.
