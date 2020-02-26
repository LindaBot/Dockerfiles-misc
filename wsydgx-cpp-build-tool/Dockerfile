FROM mcr.microsoft.com/windows/servercore:ltsc2019

ADD https://aka.ms/vs/16/release/vc_redist.x64.exe C:\\vc_redist.x64.exe
RUN C:\vc_redist.x64.exe /quiet /install /norestart

ADD https://aka.ms/vs/16/release/vs_buildtools.exe C:\\vs_buildtools.exe

ADD https://dist.nuget.org/win-x86-commandline/latest/nuget.exe C:\\nuget.exe

RUN C:\\vs_buildtools.exe --add Microsoft.VisualStudio.Component.Windows10SDK --add Microsoft.VisualStudio.Component.Windows10SDK.18362 --add Microsoft.VisualStudio.Component.Roslyn.Compiler --add Microsoft.Component.MSBuild --add Microsoft.VisualStudio.Component.CoreBuildTools --add Microsoft.VisualStudio.Workload.MSBuildTools --add Microsoft.VisualStudio.Component.VC.CoreBuildTools --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --add Microsoft.VisualStudio.Component.VC.Redist.14.Latest --add Microsoft.VisualStudio.Component.VC.CMake.Project --add Microsoft.VisualStudio.Component.TestTools.BuildTools --add Microsoft.VisualStudio.Component.VC.ATL --add Microsoft.VisualStudio.Component.VC.ATLMFC --add Microsoft.VisualStudio.Component.VC.ASAN --add Microsoft.VisualStudio.Workload.VCTools --add Microsoft.VisualStudio.Component.NuGet.BuildTools --quiet --wait

RUN setx path "%path%;C:\Program Files (x86)\Microsoft Visual Studio\2019\BuildTools\MSBuild\Current\Bin"

RUN del C:\vc_redist.x64.exe & del C:\vs_buildtools.exe
