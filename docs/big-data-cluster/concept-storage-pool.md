---
title: What is the SQL Server big data clusters storage pool? | Microsoft Docs
description: This article describes the storage pool in a SQL Server 2019 big data cluster.
author: rothja 
ms.author: jroth 
manager: craigg
ms.date: 10/01/2018
ms.topic: conceptual
ms.prod: sql
---

# What is the SQL Server big data clusters storage pool?

This article describes the role of the *SQL Server storage pool* in a SQL Server 2019 preview big data cluster. The following sections describe the architecture and functionality of a SQL storage pool.

## Storage pool architecture

The storage pool consists of storage nodes comprised of SQL Server on Linux, Spark, and HDFS. All the storage nodes in a SQL big data cluster are members of an HDFS cluster.

![Storage pool architecture](media/concept-storage-pool/scale-big-data-on-demand.png)

## Responsibilities

Storage nodes are responsible for:

- Data ingestion through Spark.
- Data storage in HDFS (Parquet format). HDFS also provides data persistency, as HDFS data is spread across all the storage nodes in the SQL big data cluster.
- Data access through HDFS and SQL Server endpoints.

## Next steps

To learn more about the SQL Server big data clusters, see the following overview:

- [What are SQL Server 2019 big data clusters?](big-data-cluster-overview.md)
