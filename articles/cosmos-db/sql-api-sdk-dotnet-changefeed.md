---
title: 'Azure Cosmos DB: .NET Change Feed Processor API, SDK & resources | Microsoft Docs'
description: Learn all about the Change Feed Processor API and SDK including release dates, retirement dates, and changes made between each version of the .NET Change Feed Processor SDK.
services: cosmos-db
documentationcenter: .net
author: ealsur
manager: kfile

ms.assetid: f2dd9438-8879-4f74-bb6c-e1efc2cd0157
ms.service: cosmos-db
ms.workload: data-services
ms.tgt_pltfrm: na
ms.devlang: dotnet
ms.topic: article
ms.date: 04/19/2018
ms.author: maquaran

---
# .NET Change Feed Processor SDK: Download and release notes
> [!div class="op_single_selector"]
> * [.NET](sql-api-sdk-dotnet.md)
> * [.NET Change Feed](sql-api-sdk-dotnet-changefeed.md)
> * [.NET Core](sql-api-sdk-dotnet-core.md)
> * [Node.js](sql-api-sdk-node.md)
> * [Async Java](sql-api-sdk-async-java.md)
> * [Java](sql-api-sdk-java.md)
> * [Python](sql-api-sdk-python.md)
> * [REST](https://docs.microsoft.com/rest/api/cosmos-db/)
> * [REST Resource Provider](https://docs.microsoft.com/rest/api/cosmos-db-resource-provider/)
> * [SQL](https://msdn.microsoft.com/library/azure/dn782250.aspx)

|   |   |
|---|---|
|**SDK download**|[NuGet](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB.ChangeFeedProcessor/)|
|**API documentation**|[Change Feed Processor library API reference documentation](/dotnet/api/microsoft.azure.documents.changefeedprocessor?view=azure-dotnet)|
|**Get started**|[Get started with the Change Feed Processor .NET SDK](change-feed.md)|
|**Current supported framework**| [Microsoft .NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653)</br> [Microsoft .NET Core](https://www.microsoft.com/net/download/core) |

## Release notes

### Stable builds

### <a name="1.3.2"/>1.3.2
* Fixes in the pending work estimation.

### <a name="1.3.1"/>1.3.1
* Stability improvements.
* Support for manual checkpointing.
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.21 and above.

### <a name="1.2.0"/>1.2.0
* Adds support for .NET Standard 2.0. The package now supports `netstandard2.0` and `net451` framework monikers.
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.17.0 and above.
* Compatible with [SQL .NET Core SDK](sql-api-sdk-dotnet-core.md) versions 1.5.1 and above.

### <a name="1.1.1"/>1.1.1
* Fixes an issue with the calculation of the estimate of remaining work when the Change Feed was empty or no work was pending.
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.13.2 and above.

### <a name="1.1.0"/>1.1.0
* Added a method to obtain an estimate of remaining work to be processed in the Change Feed.
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.13.2 and above.

### <a name="1.0.0"/>1.0.0
* GA SDK
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.14.1 and below.

### Pre-release builds

### <a name="2.0.1-prerelease"/>2.0.1-prerelease
* New v2 API:
  * Builder pattern for flexible construction of the processor: the ChangeFeedProcessorBuilder class.
    * Can take any combination of parameters.
    * Can take DocumentClient instance for monitoring and/or lease collection (not available in v1).
  * IChangeFeedObserver.ProcessChangesAsync now takes CancellationToken.
  * IRemainingWorkEstimator - the remaining work estimator can be used separately from the processor.
  * New extensibility points:
    * IParitionLoadBalancingStrategy - for custom load-balancing of partitions between instances of the processor.
    * ILease, ILeaseManager - for custom lease management.
    * IPartitionProcessor - for custom processing changes on a partition.
* Logging - uses [LibLog](https://github.com/damianh/LibLog) library.
* 100% backward compatible with v1 API.
* Compatible with [SQL .NET SDK](sql-api-sdk-dotnet.md) versions 1.21.1 and above.

## Release & Retirement dates
Microsoft will provide notification at least **12 months** in advance of retiring an SDK in order to smooth the transition to a newer/supported version.

New features and functionality and optimizations are only added to the current SDK, as such it is recommended that you always upgrade to the latest SDK version as early as possible. 

Any request to Cosmos DB using a retired SDK will be rejected by the service.

<br/>

| Version | Release Date | Retirement Date |
| --- | --- | --- |
| [1.3.2](#1.3.2) |April 18, 2018 |--- |
| [1.3.1](#1.3.1) |March 13, 2018 |--- |
| [1.2.0](#1.2.0) |October 31, 2017 |--- |
| [1.1.1](#1.1.1) |August 29, 2017 |--- |
| [1.1.0](#1.1.0) |August 13, 2017 |--- |
| [1.0.0](#1.0.0) |July 07, 2017 |--- |


## FAQ
[!INCLUDE [cosmos-db-sdk-faq](../../includes/cosmos-db-sdk-faq.md)]

## See also
To learn more about Cosmos DB, see [Microsoft Azure Cosmos DB](https://azure.microsoft.com/services/cosmos-db/) service page. 

