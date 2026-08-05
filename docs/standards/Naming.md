\# Naming Convention



> Version: 1.0



This document defines the naming conventions used throughout the Engineering Workspace.



Consistent naming improves readability, maintainability, discoverability, and AI understanding.



\---



\# Objective



A name should answer one question:



\*\*What is it?\*\*



A good name should not require additional explanation.



\---



\# General Principles



Good names are:



\- Clear

\- Specific

\- Predictable

\- Consistent



Avoid names that are:



\- Ambiguous

\- Generic

\- Misleading

\- Abbreviated without reason



\---



\# Language



All code identifiers, file names, folder names, database objects, and documentation filenames should use English.



Chinese may be used only for:



\- User interface text

\- Business documentation

\- Customer-facing content



\---



\# Class Naming



Classes represent nouns.



Use PascalCase.



Examples



```

ProductionOrder



AlarmService



DatabaseConfiguration



UserSession

```



Avoid



```

Data



Helper



Manager1



ClassA

```



\---



\# Interface Naming



Prefix with \*\*I\*\*.



Examples



```

IRepository



ILogger



ICommunicationService

```



\---



\# Method Naming



Methods represent actions.



Use verbs.



Examples



```

Connect()



LoadOrders()



SaveConfiguration()



CalculateYield()



ValidateBarcode()

```



Avoid



```

Handle()



Do()



Run()



Execute1()

```



\---



\# Property Naming



Properties represent state.



Examples



```

ConnectionState



CurrentUser



IsConnected



RetryCount

```



Boolean properties should begin with:



```

Is



Has



Can



Should

```



Examples



```

IsConnected



HasPermission



CanRetry



ShouldReconnect

```



\---



\# Variable Naming



Variables should describe their purpose.



Good



```

productionOrder



currentTemperature



retryCount

```



Avoid



```

temp



obj



item1



value



a



b

```



\---



\# Constant Naming



Use PascalCase.



Examples



```

DefaultTimeout



MaxRetryCount



DefaultPort

```



Avoid ALL\_CAPS.



\---



\# Enum Naming



Enum names should represent categories.



Examples



```

ConnectionState



MachineStatus



OrderType

```



Enum values should be singular.



```

Running



Stopped



Waiting

```



\---



\# Event Naming



Events describe completed actions.



Examples



```

ConnectionEstablished



OrderCompleted



AlarmTriggered

```



\---



\# File Naming



One public class per file.



File name must equal class name.



```

OrderService.cs



BarcodeScanner.cs



MachineController.cs

```



\---



\# Folder Naming



Folders represent responsibilities.



Examples



```

Communication



Services



Repositories



Models



Views



ViewModels



Utilities

```



Avoid



```

Temp



Misc



Other



NewFolder

```



\---



\# Database Naming



Tables use singular nouns.



Examples



```

Order



Product



Machine



Employee

```



Primary keys



```

Id

```



Foreign keys



```

OrderId



ProductId



MachineId

```



Avoid prefixes like:



```

tbl\_



tb\_



t\_

```



\---



\# Service Naming



Services should end with:



```

Service

```



Examples



```

AlarmService



UserService



ProductionService

```



\---



\# Repository Naming



Repositories end with:



```

Repository

```



Examples



```

OrderRepository



MachineRepository

```



\---



\# Communication Modules



Use protocol names directly.



Examples



```

TcpClient



SerialPortService



ModbusMaster



PlcCommunicationService

```



\---



\# UI Naming



Forms



```

LoginForm



MainForm



SettingsForm

```



Dialogs



```

ConfirmDialog



AlarmDialog

```



Controls



```

ProductionGrid



StatusPanel

```



\---



\# Configuration Naming



Configuration classes end with:



```

Configuration

```



Examples



```

DatabaseConfiguration



LoggingConfiguration



CommunicationConfiguration

```



\---



\# Avoid Generic Suffixes



Avoid names such as



```

Helper



Common



Util



Tool



Base



Manager

```



Unless their responsibility is clearly defined.



\---



\# Abbreviations



Only use industry-standard abbreviations.



Acceptable



```

PLC



MES



ERP



SQL



TCP



UDP



HTTP



API



DTO

```



Avoid project-specific abbreviations.



\---



\# Temporary Names



Never leave temporary names in committed code.



Examples



```

test



newClass



temp



temp1



demo



sample

```



Rename before commit.



\---



\# Documentation Naming



Documentation files use PascalCase.



Examples



```

Coding\_Style.md



Git\_Workflow.md



Development\_Standards.md

```



\---



\# Final Rule



A future developer should understand the purpose of a component simply by reading its name.



If the name requires explanation, choose a better name.

