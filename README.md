# unit-testing-using-dotnet-test
## What did I do
First, I created `unit-testing-using-dotnet-test` solution by following command.
```console
$ dotnet new sln -o unit-testing-using-dotnet-test
```
Then, I created class library by following command.
```console
$ dotnet new classlib -o PrimeService
```
And I renamed generated class file.
```console
$ mv PrimeService/Class1.cs PrimeService/PrimeService.cs
```
I modifed `PrimeService/PrimeService.cs` to as following.
```c#
using System;

namespace Prime.Service
{
    public class PrimeSercice
    {
        public bool IsPrime(int cadidate)
        {
            throw new NotImplementedException("Not implemented.");
        }
    }
}
```
In the `unit-testing-using-dotnet-test` directory, run the following command to added the class library project to the solution.
```console
$ dotnet sln add ./PrimeService/PrimeService.csproj
```
Created the PrimeService.Tests project by running the following command.
```console
$ dotnet new xunit -o PrimeService.Tests
```
At this point project structure as below.
```console
├── PrimeService
│   ├── PrimeService.cs
│   ├── PrimeService.csproj
│   └── obj
│       ├── PrimeService.csproj.nuget.cache
│       ├── PrimeService.csproj.nuget.dgspec.json
│       ├── PrimeService.csproj.nuget.g.props
│       ├── PrimeService.csproj.nuget.g.targets
│       └── project.assets.json
├── PrimeService.Tests
│   ├── PrimeService.Tests.csproj
│   ├── UnitTest1.cs
│   └── obj
│       ├── PrimeService.Tests.csproj.nuget.cache
│       ├── PrimeService.Tests.csproj.nuget.dgspec.json
│       ├── PrimeService.Tests.csproj.nuget.g.props
│       ├── PrimeService.Tests.csproj.nuget.g.targets
│       └── project.assets.json
└── unit-testing-using-dotnet-test.sln
```
The test fails because IsPrime hasn't been implemented. Using the TDD approach, write only enough code so this test passes. Update IsPrime with the following code:
```C#
public bool IsPrime(int candidate)
{
    if (candidate == 1)
    {
        return false;
    }
    throw new NotImplementedException("Not fully implemented.");
}
```

----

comming soon...
