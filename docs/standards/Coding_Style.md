\# Coding Style



> Version: 1.0



This document defines the coding conventions for all C#/.NET projects within the Engineering Workspace.



The objective is to maximize readability, maintainability, and long-term consistency.



\---



\# General Principles



Code is read far more often than it is written.



Every line of code should optimize for the next engineer who reads it.



Prefer:



\- Readability

\- Simplicity

\- Consistency



Avoid:



\- Clever code

\- Hidden behavior

\- Overengineering



\---



\# Naming Conventions



Follow Microsoft's official C# naming conventions.



\## Classes



Use PascalCase.



Good



```csharp

ProductionOrderService

AlarmManager

DatabaseConnection

```



Bad



```csharp

productionService

service\_alarm

Manager1

```



\---



\## Interfaces



Prefix with I.



```csharp

IRepository

ILogger

ICommunicationService

```



\---



\## Methods



Use PascalCase.



Method names should describe actions.



```csharp

LoadOrders()



Connect()



SaveConfiguration()

```



Avoid:



```csharp

Do()



Handle()



Process1()

```



\---



\## Variables



Use camelCase.



```csharp

orderCount



currentUser



connectionState

```



Avoid abbreviations unless universally understood.



Good



```csharp

productionOrder

```



Bad



```csharp

po

```



\---



\## Constants



Use PascalCase.



```csharp

DefaultTimeout



MaxRetryCount

```



Do not use ALL\_CAPS.



\---



\## Private Fields



Use `\_camelCase`.



```csharp

private readonly ILogger \_logger;



private readonly SqlConnection \_connection;

```



\---



\# File Organization



One public class per file.



File name should match class name.



Example



```

OrderService.cs



OrderRepository.cs



ProductionController.cs

```



\---



\# Project Structure



A standard industrial project should separate responsibilities.



Recommended structure



```

src/



Application/



Domain/



Infrastructure/



Communication/



Database/



Models/



Services/



Utilities/



Views/



ViewModels/

```



Do not mix UI logic with business logic.



\---



\# Method Design



A method should perform one clear responsibility.



Prefer



```csharp

LoadOrders()



ValidateOrder()



SaveOrder()

```



Avoid



```csharp

LoadValidateSaveEverything()

```



\---



\# Method Length



Prefer methods under approximately 30 lines.



Long methods usually indicate multiple responsibilities.



Extract reusable logic into private methods.



\---



\# Class Design



Each class should have a single responsibility.



If a class grows continuously,



consider splitting responsibilities.



\---



\# Exception Handling



Handle exceptions intentionally.



Good



```csharp

try

{

&#x20;   Save();

}

catch(SqlException ex)

{

&#x20;   \_logger.LogError(ex);

&#x20;   throw;

}

```



Avoid



```csharp

catch(Exception)

{

}

```



Never silently ignore exceptions.



\---



\# Logging



Log meaningful events.



Examples



\- Connection established

\- PLC disconnected

\- Database timeout

\- User login

\- Critical business failure



Avoid excessive logging.



Logs should help diagnose problems.



\---



\# Comments



Good code explains HOW.



Comments explain WHY.



Avoid obvious comments.



Bad



```csharp

// Increase i

i++;

```



Useful



```csharp

// Retry because PLC may temporarily reject the command.

```



\---



\# Magic Numbers



Avoid hard-coded numbers.



Good



```csharp

const int MaxRetry = 3;

```



Bad



```csharp

if(retry > 3)

```



\---



\# Async Programming



Prefer async/await for IO operations.



Avoid blocking calls.



Avoid



```csharp

.Result



.Wait()

```



Use



```csharp

await

```



whenever practical.



\---



\# SQL Access



Never concatenate SQL strings.



Use parameterized queries.



Separate SQL access from UI code.



Prefer repository or service layers.



\---



\# PLC / Device Communication



Communication code should be isolated.



Recommended



```

Communication/



PLC/



Serial/



TCP/



Modbus/

```



UI should never communicate with hardware directly.



\---



\# WinForms



Forms should focus on:



\- UI

\- User interaction

\- Data binding



Business logic belongs inside Services.



Database logic belongs inside Repositories.



Communication belongs inside Communication layer.



\---



\# Configuration



Avoid hard-coded paths.



Use configuration files.



Centralize configuration management.



\---



\# Dependency Management



Depend on abstractions whenever reasonable.



Avoid unnecessary coupling between modules.



\---



\# Code Reuse



Before creating new code,



search for existing implementations.



Duplicate logic should be eliminated whenever practical.



\---



\# Formatting



Use Visual Studio default formatting.



Indentation:



4 spaces.



UTF-8 encoding.



One statement per line.



One declaration per line.



\---



\# Regions



Avoid excessive use of #region.



Use regions only when they improve readability.



Do not use regions to hide poor class design.



\---



\# Definition of Good Code



Good code is:



\- Easy to read

\- Easy to modify

\- Easy to debug

\- Easy to test

\- Easy to extend



Future maintainers should understand the code without additional explanation.



\---



\# Final Rule



Always prefer readable code over clever code.



The simplest correct solution is usually the best solution.

