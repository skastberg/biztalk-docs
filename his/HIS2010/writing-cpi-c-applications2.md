---
title: "Writing CPI-C Applications2 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 54088e87-d9e4-43ef-9205-36df841ab0ca
caps.latest.revision: 3
---
# Writing CPI-C Applications
A processing task accomplished by programs using Common Programming Interface for Communications (CPI-C) is called a transaction. Consequently, programs that use CPI-C are called transaction programs (TPs). These programs communicate as peers, on an equal (rather than hierarchical) basis. The TPs use CPI-C calls to exchange status information and application data. Each TP uses CPI-C calls to supply parameters to CPI-C, which performs the preferred function and returns parameters to the TP.  
  
 TPs distributed across a local or wide area network perform distributed transaction processing.  
  
 This section describes how to write transaction programs using CPI-C and how to configure the systems on which TPs run. The topics in this section cover the following general areas:  
  
-   Understanding fundamental concepts related to TPs.  
  
-   Designing and coding TPs.  
  
-   Configuring registry and environment variables for invokable TPs.  
  
-   Configuring Microsoft® Host Integration Server to work with your TPs.  
  
 This section contains:  
  
-   [Communication Between TPs](../HIS2010/communication-between-tps-cpi-c-1.md)  
  
-   [Designing and Coding TPs](../HIS2010/designing-and-coding-tps-cpi-c-1.md)  
  
-   [Configuring Invokable TPs](../HIS2010/configuring-invokable-tps-cpi-c-2.md)  
  
-   [Configuring Host Integration Server to Support TPs](../HIS2010/configuring-host-integration-server-to-support-tps-cpi-c-2.md)  
  
-   [Simplifying CPI-C Configuration](../HIS2010/simplifying-cpi-c-configuration-cpi-c-2.md)