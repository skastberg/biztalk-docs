---
title: "Sense Codes for SDI Messages1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4b7c44e4-f063-4478-90d2-b4e4930e5ca5
caps.latest.revision: 3
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Sense Codes for SDI Messages
When the local node detects an error in a normal flow request from the host, the message is converted into a **DATAFMI** message with the system detected error indicator (SDI) set to inform the application and to allow data to be processed serially. The application must convert the message to a [Status-Acknowledge(Ack)](../HIS2010/status-acknowledge-ack-1.md) to allow the local node to send the required negative response to the host. The possible error codes delivered to the function management interface (FMI) application on such SDI messages are tabulated in the following table.  
  
 The sense codes beginning with 0x40 will only be delivered if the corresponding receive check has been enabled in the connection information control block (CICB) on the [Open(SSCP) Request](../HIS2010/open-sscp-request1.md) from the application. If a receive check has been disabled, the message can still be converted to an SDI message. For example, a message with begin bracket (BB), -begin chain (BC) would fail as 2002 or 2003 if 4003 were disabled.  
  
 When the application uses a **Status-Control(LUSTAT) Request** to reject outbound data, the sense codes supplied by the application will be present on the SDI message generated by the local node. For more information, see [LUSTATs](../core/lustats]1.md).  
  
|Sense code|Description|  
|----------------|-----------------|  
|0x0809|Mode inconsistency.|  
|0x080B|Bracket race error.|  
|0x081B|Contention race condition.|  
|0x1003|Incorrect FM profile for request.|  
|0x2001|Sequence number error.|  
|0x2002|Chaining error.|  
|0x2003|Bracket error.|  
|0x2004|Direction error.|  
|0x2006|Data traffic quiesced.|  
|0x4003|BB not allowed.|  
|0x4004|End bracket (EB) not allowed.|  
|0x4006|Exception response not allowed.|  
|0x4007|Definite response not allowed.|  
|0x4009|Change direction (CD) not allowed.|  
|0x400B|Chaining not supported.|  
|0x400C|Brackets not supported.|  
|0x400D|CD not supported.|  
|0x400F|Incorrect use of FI.|  
|0x4011|Incorrect use of RU category.|  
|0x4014|Incorrect use of definite response 1 (DR1), definite response 2 (DR2), exception response (ER).|