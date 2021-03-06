---
title: "AdGroupBidding object"
description: "Contains the methods for specifying the ad group's bid values."
author: "brapel"
manager: ehansen

ms.author: "v-brapel"
ms.service: "bingads-scripts"
ms.topic: "article"
---

# AdGroupBidding

Contains the methods used to manage an ad group's bid values.

## Methods
|Method Name|Return Type|Description|
|-|-|-
[getCpc](#getcpc)|double|Gets the ad group's CPC bid.
[setCpc(double cpc)](#setcpc-double-cpc-)|void|Sets the ad group's CPC bid.


## <a name="getcpc"></a>getCpc
Gets the ad group's CPC bid amount. 

### Returns
|Type|Description|
|-|-
double|The ad group's maximum CPC bid amount.

## <a name="setcpc-double-cpc-"></a>setCpc(double cpc)
Sets the ad group's CPC bid amount. 

Specifies the bid amount to use when the keyword matches the user's search term and the ad group's bid strategy is MANUAL_CPC. Bing uses this bid if a lower-level entity such as keyword does not override it.

If you specify a bid value that's not valid, the call silently fails. To confirm whether the bid was updated, you must get the object again and test whether the property's value equals the new value. For information, see [Handling errors and warnings](../concepts/errors-and-warnings.md).

### Arguments
|Name|Type|Description|
|-|-|-
cpc|double|The ad group's maximum CPC bid. The account's currency determines the minimum and maximum bid values. For more information, see [Bid and budget currencies](/bingads/guides/currencies#bidandbudget).

### Returns
|Type|Description|
|-|-
void|Returns nothing.


## See also

[AdGroup.bidding()](AdGroup.md#bidding)