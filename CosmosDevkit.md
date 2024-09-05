# How to install CosmosOS Devkit
## Prerequisites
- Windows10/11 or linux
- [.Net6](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- [vcpp2010](https://www.microsoft.com/en-us/download/details.aspx?id=26999&msockid=19eaa39fc49d6d381175b70dc57c6c43)
- [VisualStudio2022 (windows only)](https://visualstudio.microsoft.com/en-us/downloads/)

## Instaling the workloads (you do not need vs2022 if you are on linux)
Cosmos requires a workload for visual studio to work...
To install it you select the ExtensionsDevelopment workload in the visual studio installer before
installing visual studio 2022 or if you already have it installed you can
modify the install and add the workload.

![workload](workloads.png)

## downloading the devkit
if you have git installed run this command in an empty folder
```
git clone https://github.com/CosmosOS/Cosmos.git
```
else you can go to the [CosmosOS](https://github.com/CosmosOS/Cosmos.git) repo and clone it manually... tho remember to put it
in an empty folder.

after cloning the repo you need to rename the Cosmos-master folder to Cosmos.

## building the devkit
### Windows
run the install-VS2022.bat file with adiministrator privileges and make sure to have visual studio closed.
### Linux
change line 19 from
```
BUILDMODE=Release
```
to
```
BUILDMODE=Debug
```
and open a terminal in the Cosmos folder and run the make command.
you might want to also install the cosmos template... install it you just run
```
dotnet new install source/templates/csharp
```
optionally you can install [CosmosCLI](https://github.com/PratyushKing/CosmosCLI) for better project management on linux.