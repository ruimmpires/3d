# 3d
3d projects

## 1. 3D Printer
Creality Ender-3 V3 SE ordered and to get delivered 4 Nv 2025. Paid 170€.

## 2. Examples
Asked Gemini :-)
Registed and got account in https://www.thingiverse.com/. Downloaded a couple of examples well structured:
* images
* stl files
* readme and license

### 2.1 

## 3. Design
Asked gemini :-)
Started using https://www.tinkercad.com/ and found that it is not that easy.


### 3.1 Box1_USB_power


## 4. Slicer
Asked gemini :-)
Started using Iltimaker Cura. Downloaded from https://ultimaker.com/software/ultimaker-cura/.

### 4.1 Installation in Kali Linux
Almost a nightmare, but Gemini helped a lot. The answers were not easy to find so I gave up and trusted AI.
```
└─$ ./UltiMaker-Cura-5.11.0-linux-X64.AppImage
UM/Settings/SettingFunction.py:244: DeprecationWarning: ast.Str is deprecated and will be removed in Python 3.14; use ast.Constant instead
  def visit_Str(self, node: ast.Str) -> None:
qt.glx: qglx_findConfig: Failed to finding matching FBConfig for QSurfaceFormat(version 4.1, options QFlags<QSurfaceFormat::FormatOption>(), depthBufferSize -1, redBufferSize 1, greenBufferSize 1, blueBufferSize 1, alphaBufferSize -1, stencilBufferSize -1, samples -1, swapBehavior QSurfaceFormat::SingleBuffer, swapInterval 1, colorSpace QColorSpace(), profile  QSurfaceFormat::CoreProfile)
qt.glx: qglx_findConfig: Failed to finding matching FBConfig for QSurfaceFormat(version 4.1, options QFlags<QSurfaceFormat::FormatOption>(), depthBufferSize -1, redBufferSize 1, greenBufferSize 1, blueBufferSize 1, alphaBufferSize -1, stencilBufferSize -1, samples -1, swapBehavior QSurfaceFormat::SingleBuffer, swapInterval 1, colorSpace QColorSpace(), profile  QSurfaceFormat::CoreProfile)
Could not initialize GLX
zsh: IOT instruction (core dumped)  ./UltiMaker-Cura-5.11.0-linux-X64.AppImage
```
The solution:
Download the correct package: Use this new link to get the 4.8.12-3.1 version.
```
wget http://ftp.debian.org/debian/pool/main/z/z3/libz3-4_4.8.12-3.1_amd64.deb
```
Extract the package:
```
dpkg-deb -x libz3-4_4.8.12-3.1_amd64.deb .
```
Run Cura with the LD_LIBRARY_PATH: This step is the same as before.
```
LD_LIBRARY_PATH=~/cura_lib/usr/lib/x86_64-linux-gnu ./UltiMaker-Cura-5.11.0-linux-X64.AppImage
```
This should successfully find the library and resolve the GLX error.

### 4.2 Usage
The designs are stored online https://digitalfactory.ultimaker.com. Not a simple environment, but maybe I need to learn.

