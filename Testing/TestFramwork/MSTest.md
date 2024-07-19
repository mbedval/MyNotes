
[MSTest](https://www.nuget.org/packages/MSTest.Sdk) is Microsoft supported Test Framework. The MSTest runner is a lightweight and portable alternative to [VSTest](https://github.com/microsoft/vstest) for running tests in all contexts (for example, continuous integration (CI) pipelines, CLI, Visual Studio Test Explorer, and VS Code Text Explorer).
The MSTest runner is open source, and builds on a [`Microsoft.Testing.Platform`](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-platform-intro) library. You can find `Microsoft.Testing.Platform` code in [microsoft/testfx](https://github.com/microsoft/testfx/tree/main/src/Platform/Microsoft.Testing.Platform) GitHub repository.



This package includes a custom test SDK for writing tests with MSTest.

```
dotnet add package MSTest.Sdk --version 3.5.0
```

#### runsettings

The MSTest runner supports the [runsettings](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-platform-extensions-vstest-bridge#runsettings-support) through the command-line option `--settings`. For the full list of supported MSTest entries, see [Configure MSTest: Runsettings](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-mstest-configure#runsettings). The following commands show various usage examples.

### MSTest Example
```
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace MSTestNamespace
{
    [TestClass]
    public class UnitTest1
    {
        [TestMethod, Priority(1), TestCategory("CategoryA")]
        public void TestMethod1()
        {
        }

        [TestMethod, Priority(2)]
        public void TestMethod2()
        {
        }
    }
}
```

###  Annotations 

|              |     |
| ------------ | --- |
| TestMethod   |     |
| Priority     |     |
| TestCategory |     |

### Execute Select Testcase

```
dotnet  test --filter Method  
// runs only test containing 'method' in name

dotnet test --filter Name~TestMethod 
//runs only test with  name

dotnet test --filter ClassName=NameSpace.UnitTest1 

dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1
// run all test except 

dotnet test --filter TestCategory=CategoryA
//Runs tests that are annotated with `[TestCategory("CategoryA")]`.


dotnet test --filter Priority=2
// run all test with annotation based on priority filtering
```