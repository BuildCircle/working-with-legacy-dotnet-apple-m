# Working with legacy dotnet on Apple M chips 

1. Parallels

Download and install parallels here https://www.parallels.com/products/desktop/download/

2. Windows 11 for ARM

This is conveniently installed via Parallels, nothing to download here.

3. Visual Studio & .NET Framework for ARM

The Visual Studio installer will install the .NET framework for ARM when you select Desktop or Web workloads
https://visualstudio.microsoft.com/downloads/

4. TFSVC & Team Foundation Explorer 

TFS team explorer is an older version of Visual Studio cut back just for navigating TFSVC, this was built for x86 and will run on Windows 11 emulation layer. When installed it will give performance warnings but functions as expected as of April 2024
(Installer in this repository)

5. Test your setup (Requires a Build Circle account)

Try and connect to this TFSVC repository, build, and run the .NEt Framework app to test everything is working.
https://dev.azure.com/buildcircle/legacy-dotnet-application

6. SQL Server

As of April 2024 there is no native build of SQL Server for ARM on any OS, Below are the current workarounds
* Option 1: docker, an x86 image running on Rosetta 2
https://hub.docker.com/_/microsoft-mssql-server

* Option 2: custom install script, installing SQL Server on Windows 11 using Windows x86 emulation layer
https://github.com/jimm98y/MSSQLEXPRESS-M1-Install
