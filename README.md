# C# Repository Template

Repository template for a C# project.

## Getting Started

- Create a new repository on GitHub and choose this repository as the template, or click on the _"Use this template"_ button on the repository home page.
- Rename the solution file in the root of the repository (`RENAME-ME.sln`).
- Update `Directory.Build.props` in the root folder and replace the placeholder values in the shared project properties (e.g. `{{COPYRIGHT_START_YEAR}}`).
- Create new library and application projects in the `src` folder.
- Create test and benchmarking projects in the `test` folder.
- Create example projects that demonstrate the library and application projects in the `samples` folder.

## Repository Structure

The repository is organised as follows:

- `[root]`
  - `[build]`
    - `Dependencies.props` - Common NuGet package versions.
    - `Get-Version.ps1` - PowerShell script to retrieve assembly version, file version, etc. to use when building C# projects.
    - `NetFX.targets` - Adds package references for building projects that target .NET Framework on non-Windows systems.
    - `Set-TeamCityParameters.ps1` - PowerShell script that can be called from TeamCity to set the build version and various agent parameters at build time.
    - `Tools.ps1` - Helper functions used by `build.ps1`.
    - `version.json` - Defines version numbers used when building the projects.
  - `[samples]` - Example projects to demonstrate the usage of the repository libraries and applications.
    - `Directory.Build.props` - Common MSBuild properties and targets related to example projects (see [here](https://docs.microsoft.com/en-us/visualstudio/msbuild/customize-your-build) for details).
  - `[src]` - Source code for repository libraries and applications.
  - `[test]` - Test and benchmarking projects.
    - `Directory.Build.props` - Common MSBuild properties and targets related to test projects (see [here](https://docs.microsoft.com/en-us/visualstudio/msbuild/customize-your-build) for details).
  - `.editorconfig` - Code style rules (see [here](https://editorconfig.org/) for details).
  - `.gitattributes`
  - `.gitignore`
  - `build.ps1` - PowerShell script to assist with building the projects from the command line.
  - `Directory.Build.props` - Common MSBuild properties and targets (see [here](https://docs.microsoft.com/en-us/visualstudio/msbuild/customize-your-build) for details).
  - `Directory.Build.targets` - Common MSBuild properties and targets (see [here](https://docs.microsoft.com/en-us/visualstudio/msbuild/customize-your-build) for details). 
  - `README.md`
  - `RENAME-ME.sln` - Empty Visual Studio solution file.
