FROM mcr.microsoft.com/windows/servercore:ltsc2019

ADD https://download.visualstudio.microsoft.com/download/pr/7d6389b7-eda7-4ae0-924d-4fedaa3d0fc7/7712bebba5b34149837f9b60928acbb1/dotnet-sdk-3.0.102-win-x64.exe /dotnet-sdk-3.0.102-win-x64.exe 
ADD https://aka.ms/vs/16/release/vc_redist.x64.exe /vc_redist.x64.exe

RUN C:\dotnet-sdk-3.0.102-win-x64.exe /quiet /install
RUN C:\vc_redist.x64.exe /quiet /install /norestart

RUN del C:\vc_redist.x64.exe & del C:\dotnet-sdk-3.0.102-win-x64.exe