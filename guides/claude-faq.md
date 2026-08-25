## Claude FAQ

Use this FAQ to help you set set up for Claude for our class. We're building this document as we go, so if you face any issues not covered here, 
please let the teacher staff know, so that we can improve the documentation. 

## Table of Contents
* [1. Test Claude access](#1)
* [2. Install Claude Code](#2)
* [3. Troubleshooting claude not found / claude is not recognized errors](#3)

### <a id="1"></a>1. Test Claude access

Go to [claude.ai](claude.ai)
Log in with yourEID@eid.utexas.edu

If you have any access issues, reach out to UT's 


### <a id="2"></a>2. Install Claude Code

On MacOS:
```
brew install --cask claude-code
claude --version
claude
/login
/exit
```

On Windows:

Open a Windows PowerShell and run:
```
irm https://claude.ai/install.ps1 | iex
```
Close and open a new shell, then run:

```
claude
```
Log in by following the browser prompts. 

```
/exit
```

Note When you log in, use yourEID@eid.utexas.edu, just like when you accessed [claude.ai](claude.ai). 


### <a id="3"></a>3. Troubleshooting claude not found / claude is not recognized errors 

On MacOS:
```
brew list --cask claude-code
eval "$(/opt/homebrew/bin/brew shellenv)"
source ~/.zprofile
```

On Windows:
```
Test-Path "$env:USERPROFILE\.local\bin\claude.exe"
```

If the previous command returns True, then run to add the location to your path:
```
$currentPath = [Environment]::GetEnvironmentVariable('PATH', 'User')
[Environment]::SetEnvironmentVariable('PATH', "$currentPath;$env:USERPROFILE\.local\bin", 'User')
```
