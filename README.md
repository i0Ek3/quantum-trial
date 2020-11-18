# quantum-trial

## Run & Build

`dotnet build ; dotnet run`

## Q & A

Problem we have met: 

`MSBUILD : error MSB1003: Specify a project or solution file. The current working directory does not contain a project or solution file.`

The reason is there is a need for a .csproj file to fetch info to build, but we don't have the file. So we recreated a Q# project using VS Code, and now we have this file. After then, you will see follows log message, that's means you can build it successful:

```
quantum-trial/quantum [master●] » dotnet build
Microsoft (R) Build Engine version 16.7.1+52cd83677 for .NET
Copyright (C) Microsoft Corporation. All rights reserved.

  Determining projects to restore...
  Restored /xxx/quantum-trial/quantum/quantum.csproj (in 530 ms).
/xxx/quantum-trial/quantum/Program.qs(35,18): warning QS5002: This expression may be short-circuited, and operation calls may not be executed. [/xxx/quantum-trial/quantum/quantum.csproj]

  ____________________________________________

  Q#: Success! (0 errors, 1 warning)

  quantum -> /xxx/quantum-trial/quantum/bin/Debug/netcoreapp3.1/quantum.dll

Build succeeded.

/xxx/quantum-trial/quantum/Program.qs(35,18): warning QS5002: This expression may be short-circuited, and operation calls may not be executed. [/xxx/quantum-trial/quantum/quantum.csproj]
    1 Warning(s)
    0 Error(s)

Time Elapsed 00:00:15.70
```

## Reference

- [https://docs.microsoft.com/zh-cn/quantum/quickstarts/install-python?tabs=tabid-dotnetcli](https://docs.microsoft.com/zh-cn/quantum/quickstarts/install-python?tabs=tabid-dotnetcli)
