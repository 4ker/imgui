
```bash
@REM Build for Visual Studio compiler. Run your copy of vcvars32.bat or vcvarsall.bat to setup command-line compiler.
mkdir Debug
set DXSDK_DIR=C:/Program Files (x86)/Microsoft SDKs/Windows/v7.0A
set DXSDK_INCLUDE_DIR=%DXSDK_DIR%/Include
set DXSDK_LIB_DIR=%DXSDK_DIR%/Lib

%comspec% /c"c:\Program Files (x86)\Microsoft Visual Studio 10.0\VC\vcvarsall.bat" amd64 && cl.exe /nologo /Zi /MD /I ..\..\src\ImGui /I "%DXSDK_INCLUDE_DIR%" /D UNICODE /D _UNICODE *.cpp ..\..\src\ImGui\*.cpp /FeDebug/directx9_example.exe /FoDebug/ /link /LIBPATH:"%DXSDK_LIB_DIR%" d3d9.lib
```

[Download DirectX Software Development Kit from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/confirmation.aspx?id=6812)
