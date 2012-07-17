Visual Studio Git Ignore
=====================

A better .gitignore file for Visual Studio from NuGet.

## How to use
This project is <a href="http://nuget.org/packages/VisualStudioGitIgnore">published as a NuGet Package</a>. When you install this package, it will add a git.ignore file to your project. Open that file and read its contents for further instructions.

## How to generate the nupkg file
After getting the source, build it in Release mode. Next, open the Package Manager Console and switch to the csproj folder:

    PM> dir

            Directory: C:\Path\To\VisualStudioGitIgnore

    Mode                LastWriteTime     Length Name
    ----                -------------     ------ ----
    d----         7/17/2012   1:37 AM            VisualStudioGitIgnore
    -a---         7/17/2012   1:31 AM        790 .gitignore
    -a---         7/17/2012   1:38 AM        249 README.md
    -a---         7/17/2012   1:19 AM       1212 VisualStudioGitIgnore.sln

    PM> cd VisualStudioGitIgnore
    PM> dir

            Directory: C:\Code\GitHub\VisualStudioGitIgnore\VisualStudioGitIgnore

    Mode                LastWriteTime     Length Name
    ----                -------------     ------ ----
    d----         7/17/2012   1:19 AM            bin
    d----         7/17/2012   1:27 AM            content
    d----         7/17/2012   1:19 AM            obj
    d----         7/17/2012   1:19 AM            Properties
    -a---         7/17/2012   1:37 AM       5259 VisualStudioGitIgnore.0.1.4581.855.nupkg
    -a---         7/17/2012   1:36 AM       2419 VisualStudioGitIgnore.csproj
    -a---         7/17/2012   1:21 AM        227 VisualStudioGitIgnore.csproj.user
    -a---         7/17/2012   1:28 AM        892 VisualStudioGitIgnore.nuspec

Once in the .csproj file's directory, package the project in release mode:

    PM> nuget pack -Prop Configuration=Release
    Attempting to build package from 'VisualStudioGitIgnore.csproj'.
    Packing files from 'C:\Path\To\VisualStudioGitIgnore\VisualStudioGitIgnore\bin\Release'.
    Using 'VisualStudioGitIgnore.nuspec' for metadata.
    Successfully created package 'C:\Path\To\VisualStudioGitIgnore\VisualStudioGitIgnore\VisualStudioGitIgnore.maj.min.build.rev.nupkg'.