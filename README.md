# QSAR Molecular Visualization Tool

This repository contains a modern, user-friendly Streamlit web application for interactive 3D visualization of **212 PFAS ligand-receptor complexes** with ERα and ERβ receptors. All data and results for these receptor-ligand structures are included—no setup or data preparation required!

## 🚀 Quick Start (3 Steps)

1. **Download & Extract**: Clone or download this repository
2. **Install Python**: Ensure you have Python 3.9+ installed
3. **Run the App**: Choose your preferred method below

### **Method 1: One-Click Launch (Windows)**
```bash
# Double-click this file or run in Command Prompt:
run_app.bat
```

### **Method 2: PowerShell (Windows)**
```bash
# Right-click and "Run with PowerShell" or run in PowerShell:
.\run_app.ps1
```

### **Method 3: Manual Installation**
```bash
# Install dependencies
pip install -r requirements.txt

# Launch application
streamlit run qsar_web_app.py
```

4. **Open your browser** to `http://localhost:8501`

## 📊 What You Get

* **3D visualization** of all 212 PFAS ligand-receptor complexes using NGL Viewer
* **Interactive selection** between ERα and ERβ receptors
* **Dataset selection** between "Commonly Exposed Set" (CE) and "Top 50 Set" (T50)
* **Real-time molecular structure viewing** with customizable representations
* **Ready-to-use**: just install dependencies and launch the app

## 📁 Included Data

* The project contains all 212 receptor-ligand complex structures in four main folders:
  * **Alpha_CE_Combined/**: 55 ERα receptor complexes (Commonly Exposed Set)
  * **Beta_CE_Combined/**: 55 ERβ receptor complexes (Commonly Exposed Set)  
  * **Alpha_T50_Combined/**: 51 ERα receptor complexes (Top 50 Set)
  * **Beta_T50_Combined/**: 51 ERβ receptor complexes (Top 50 Set)
* Each folder contains PDB files with combined receptor-ligand structures
* The app is preconfigured to use this data—no changes needed

## 🎯 Features

### Interactive 3D Structure Viewer
* **NGL Viewer integration** for high-quality molecular visualization
* **Multiple representation options**: cartoon, ball+stick, surface
* **Ligand highlighting** with automatic detection and visualization
* **Responsive design** that works on desktop and mobile devices

### Receptor Selection
* **ERα (Estrogen Receptor Alpha)**: Red-themed interface
* **ERβ (Estrogen Receptor Beta)**: Teal-themed interface
* **Side-by-side comparison** capabilities

### Dataset Options
* **Commonly Exposed Set (CE)**: 55 PFAS ligands commonly found in environmental samples
* **Top 50 Set (T50)**: 51 PFAS ligands with highest predicted binding affinities

### User Interface
* **Modern, responsive design** with gradient backgrounds
* **Intuitive navigation** with sidebar controls
* **Real-time structure loading** and visualization
* **Professional styling** with custom CSS

## 🔧 System Requirements

### Minimum Requirements
* **Python 3.9+** (recommended: 3.10 or 3.11)
* **4GB RAM** (8GB recommended for smooth performance)
* **Modern web browser** with WebGL support
* **Internet connection** for NGL Viewer library loading

### Supported Operating Systems
* **Windows 10/11** (tested and optimized)
* **macOS 10.15+** (should work with manual installation)
* **Linux** (Ubuntu 18.04+, should work with manual installation)

## 📋 Installation Guide

### For Windows Users (Recommended)
1. **Download the repository** (green "Code" button → "Download ZIP")
2. **Extract the ZIP file** to a folder of your choice
3. **Double-click `run_app.bat`** - this will automatically:
   - Install Python dependencies
   - Launch the application
   - Open your browser

### For Advanced Users
1. **Clone the repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/QSAR-Molecular-Visualization-GUI.git
   cd QSAR-Molecular-Visualization-GUI
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the application**:
   ```bash
   streamlit run qsar_web_app.py
   ```

## 🎮 Usage Instructions

1. **Start the application** using any method above
2. **Open your browser** and navigate to `http://localhost:8501`
3. **Select your preferences**:
   - Choose receptor type (ERα or ERβ)
   - Select dataset (CE or T50)
   - Pick a specific ligand from the dropdown
4. **Explore the 3D structure**:
   - Rotate, zoom, and pan the molecular viewer
   - Toggle between different molecular representations
   - Examine ligand-receptor interactions

## 🏗️ Technical Details

### Architecture
* **Frontend**: Streamlit web interface
* **3D Visualization**: NGL Viewer (WebGL-based)
* **Data Processing**: Python pathlib for file management
* **Caching**: Streamlit's built-in caching for performance

### Data Flow
1. **Data Loading**: App scans the four main data directories
2. **Ligand Detection**: Automatic identification of ligand molecules in PDB files
3. **Visualization**: Interactive 3D views generated with NGL Viewer
4. **User Interaction**: Real-time selection and display updates

### File Structure
```
QSAR-GUI-Project/
├── qsar_web_app.py          # Main Streamlit application
├── requirements.txt         # Python dependencies
├── README.md               # This file
├── run_app.bat             # Windows batch script
├── run_app.ps1             # PowerShell script
├── Alpha_CE_Combined/      # 55 ERα CE complexes
├── Beta_CE_Combined/       # 55 ERβ CE complexes
├── Alpha_T50_Combined/     # 51 ERα T50 complexes
└── Beta_T50_Combined/      # 51 ERβ T50 complexes
```

## 🌐 Browser Compatibility

* **Chrome/Chromium**: Full support ✅
* **Firefox**: Full support ✅
* **Safari**: Full support ✅
* **Edge**: Full support ✅
* **Mobile browsers**: Responsive design support ✅

## ⚡ Performance

* **Fast loading**: Optimized file structure and caching
* **Smooth visualization**: WebGL-accelerated 3D rendering
* **Responsive interface**: Real-time updates and interactions
* **Memory efficient**: Lazy loading of molecular data

## 🔧 Troubleshooting

### Common Issues & Solutions

1. **App won't start**
   - ✅ **Solution**: Ensure Python 3.9+ is installed
   - ✅ **Check**: Run `python --version` in terminal

2. **3D viewer not loading**
   - ✅ **Solution**: Enable WebGL in your browser
   - ✅ **Check**: Visit `chrome://gpu/` (Chrome) to verify WebGL

3. **Slow performance**
   - ✅ **Solution**: Close other browser tabs
   - ✅ **Solution**: Check internet connection for NGL Viewer

4. **File not found errors**
   - ✅ **Solution**: Ensure all four data folders are present
   - ✅ **Check**: Verify folder structure matches README

5. **Permission errors (Windows)**
   - ✅ **Solution**: Run Command Prompt as Administrator
   - ✅ **Alternative**: Use PowerShell instead

### Getting Help
* Check the browser console for JavaScript errors (F12)
* Verify all dependencies are installed correctly
* Ensure file paths are correct for your system
* Check that all 212 PDB files are present in the data folders

## 🎨 Customization

### Adding New Ligands
1. Place new PDB files in the appropriate folder structure
2. Ensure file naming follows the expected pattern
3. Restart the application to load new data

### Modifying Visualizations
* Edit the NGL Viewer parameters in `qsar_web_app.py`
* Customize the CSS styling for different themes
* Add new representation options

### Extending Functionality
* Add new analysis features
* Implement additional visualization options
* Create new data export capabilities

## 🤝 Contributing

To extend the application:

1. Fork the repository
2. Add new features or improvements
3. Update documentation
4. Submit pull request

## 📄 License

This application is designed for research and educational use. Please cite the original analysis when using this data.

## 📞 Contact

For questions or issues: Contact the development team

---

## 🎯 **Ready to Use!**

This application provides interactive visualization of PFAS ligand-receptor complexes for research and educational purposes. The molecular structures represent computational docking results and should be validated experimentally for research applications.

**No additional setup required** - just download, run, and explore! 🚀 