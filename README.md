# x86 .NET native compilation error
## Set up
Any UWP application that references the nuget package `ImageSharp v1.0.0-beta0002` cannot be built using the .NET Native compiler targeting the x86 platform.

Native compilations targeting the ARM and x64 platforms are successful.

Tested using the latest version of `Microsoft.NETCore.UniversalWindowsPlatform`, v6.0.6, and the latest versions of Visual Studio 2017:
- 15.6.0 Preview 2.0
- 15.5.3

## Steps to reproduce
1. Clone this repo and open the `App1.sln` in Visual Studio 2017
1. Ensure that the build configuration is set to `Release` and `x86`
1. Build the solution - the following error will be reported:

Severity|Code|Description|Project|File|Line|Suppression State
-|-|-|-|-|-|-|
Error||Internal compiler error: Object reference not set to an instance of an object.|App1|||
