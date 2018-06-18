# UpdateJava
Cleans up Java on a computer.  Old versions are removed and only the current version is installed.

## Background
Java must be installed in many enterprise environments.  Unfortunately, deploying it and keeping it maintained is a nightmare.  All too often a computer ends up with multiple legacy (i.e. vulnerable) versions.  Wouldn't it be nice to just hit a button and have all old versions of Java removed then the latest version of automatically installed?  This script attempts to solve that problem in both a SCCM and interactive environment.

## Attribution
This script is highly dependent on the very awesome PowerShell App Deployment Toolkit http://psappdeploytoolkit.com/

## Using

### Preparation
1. Download the latest Windows Offline installation executable in both 32-bit and 64-bit format from Oracle.  https://java.com/en/download/manual.jsp
2. Rename them to JavaX32.exe and JavaX64.exe and place them in the "Files" directory
3. Edit Deploy-Application.ps1 and change the Java build number to match the version you are deploying.
4. Test!

### Deploying
* Deploy using your favorite method.  Works great with SCCM or interactively.  All you need to do is run "runme.exe"

## Notes
* This script installs both the 32-bit and 64-bit of Java which are often needed in an Enterprise environment.  Why both?  Some apps and browsers use the 32-bit version while some use the 64-bit version.  It's just easier to install them both.
