
# DtiStudio for Mac OS


The DtiStudio Software package is an application for MRI visualization, tensor calculation, and tractography developed for Microsoft Visual Studio. It is designed to run on Microsoft Windows operating systems. Running Windows executables like DtiStudio.exe directly on macOS is not natively supported due to differences in operating system architectures. To use it on macOS, follow the procedures listed below.<br>

**Author**: [Kenichi Oishi](https://www.hopkinsmedicine.org/profiles/details/kenichi-oishi) MD, PhD<br>
The Russell H. Morgan Department of Radiology and Radiological Science, The Johns Hopkins University School of Medicine, Baltimore, MD, USA <br>
Department of Neurology, The Johns Hopkins University School of Medicine, Baltimore, MD, USA <br>
The Richman Family Precision Medicine Center of Excellence in Alzheimer's Disease, Johns Hopkins University School of Medicine, Baltimore, MD, USA<br>


## Version
| Version | Release Date  | 
|---------|---------------|
| 1.0.0   | January  2025 | 


## Supplementary information
DtiStudio is part of the [MRIStudio Suite](https://www.mristudio.org), which is an image processing program running under Windows. It is suitable for such tasks as tensor calculation, color mapping, fiber tracking, and 3D visualization. Most of operations can be done with only a few clicks.
Tools in the program can be grouped in the following way:

* Image Viewer
* Diffusion Tensor Calculations
* Fiber Tracking and Editing
* 3D Visualization
* Image File Management
* Region of Interesting (ROI) Drawing and Statistics
* Image Registration

## Citation
DtiStudio: resource program for diffusion tensor computation and fiber bundle tracking <br>
Hangyi Jiang, Peter C M van Zijl, Jinsuh Kim, Godfrey D Pearlson, Susumu Mori<br>
Comput Methods Programs Biomed. 2006 Feb;81(2):106-16.  doi: 10.1016/j.cmpb.2005.08.004. Epub 2006 Jan 18.<br>
(https://www.sciencedirect.com/science/article/pii/S0169260705002348?via%3Dihub)

## Instructions
1. **Install Homebrew (if not already installed)** <br>
Open the Terminal and run:<br>
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
   Follow the on-screen instructions to complete the installation.<br>
Update Homebrew:
```
brew update
```

2. **XQuartz Installation**<br>
   Wine requires XQuartz for graphical interface support. Install it via Homebrew:<br>
```
brew install --cask xquartz
```
  
3. **Install Wine**<br>
   After installing XQuartz, proceed to install Wine:
```
brew install --cask --no-quarantine wine-stable
```
Check if Wine is installed by running:
```
wine --version

```
4. **Install Rosetta 2**<br>
Apple Silicon Macs (M1/M2/M3/M4 chips): Wine is designed for x86 architecture, so running certain Windows applications may require Rosetta 2. You can install Rosetta 2 by running:
```
softwareupdate --install-rosetta
```
5. **Dowonoad DtiStudio.exe**<br>
   For general users, here is the link (https://www.mristudio.org)<br>
   **for JHU-BME students:** get DtiStudio_64_Apr_2019.exe and sample data from (https://drive.google.com/drive/folders/1wxxKQ5bRUoK3G5c2KRl6TVHtmbdCpSHO?usp=share_link). Put them under Mackintosh HD/Users/<your_account>/MRIStudio/ <br>
    
7. **Run DtiStudio on your Mac**<br>
Go to Launchpad, click Wine Stable icon to open Wine zsh.<br>
To run the installed application:<br>
Locate the .exe file inside the installed directory.<br>
Use the wine command to run vcredist_x64.exe:<br>
```
wine vcredist_x64.exe
```
then open DtiStudio<br>
```
wine DtiStudio.exe
```
