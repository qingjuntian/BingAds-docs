---
title: "BingAdsApp object"
description: "The top-level object that you use to navigate all entities in a single user account."
author: "brapel"
manager: ehansen

ms.author: "v-brapel"
ms.service: "bingads-scripts"
ms.topic: "article"
---

# BingAdsApp

This is the top-level object of Bing Ads Scripts. Use it to navigate all entities in a single user account.

## Methods

|Method Name|Return Type|Description|
|-|-|-
[adGroups](#adgroups)|[AdGroupSelector](./AdGroupSelector.md)|Gets a [selector](../concepts/selectors.md) that returns all ad groups in this account.
[campaigns](#campaigns)|[CampaignSelector](./CampaignSelector.md)|Gets a selector that returns all campaigns in this account.
[keywords](#keywords)|[KeywordSelector](./KeywordSelector.md)|Gets a selector that returns all keywords in this account.
[negativeKeywordLists](#negativekeywordlists)|[NegativeKeywordListSelector](./NegativeKeywordListSelector.md)|Gets a selector that returns  all negative keyword lists in this account.
[newNegativeKeywordListBuilder](#newnegativekeywordlistbuilder)|[NegativeKeywordListBuilder](./NegativeKeywordListBuilder.md)|Gets a builder that you use to add a negative keyword list to this account.

<!--
[ads](#ads)|[AdSelector](./AdSelector)|Returns a selector of all ads in this account.<br />
[getExecutionInfo](#getexecutioninfo)|[ExecutionInfo](./ExecutionInfo)|Returns information about the environment in which the script is currently executing.
-->


## <a name="adgroups"></a>adGroups

Gets a [selector](../concepts/selectors.md) that returns all ad groups in this account. 

### Returns

|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector.md)|A selector that returns all ad groups in the current account. Use the selector's methods to filter the list of ad groups.

<!--
## <a name="ads"></a>ads
Returns a selector of all ads in this account.


### Returns:
|Type|Description|
|-|-
[AdSelector](./AdSelector)|Selector of all ads in this account.
-->

## <a name="campaigns"></a>campaigns

Gets a [selector](../concepts/selectors.md) that returns all campaigns in this account. 

### Returns

|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector.md)|A selector that returns all campaigns in the current account. Use the selector's methods to filter the list of campaigns.

<!--
## <a name="getexecutioninfo"></a>getExecutionInfo
Returns information about the environment in which the script is currently executing.

### Returns:
|Type|Description|
|-|-
[ExecutionInfo](./ExecutionInfo)|Information about the environment in which the script is currently executing.
-->

## <a name="keywords"></a>keywords

Gets a [selector](../concepts/selectors.md) that returns all keywords in this account.

### Returns

|Type|Description|
|-|-
[KeywordSelector](./KeywordSelector.md)|A selector that returns all keywords in the current account. Use the selector's methods to filter the list of keywords.

## <a name="negativekeywordlists"></a>negativeKeywordLists

Gets a [selector](../concepts/selectors.md) that returns all negative keyword lists in this account. 

### Returns

|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector.md)|A selector that returns all negative keyword lists in the current account. Use the selector's methods to filter the list of negative keyword lists.

## <a name="newnegativekeywordlistbuilder"></a>newNegativeKeywordListBuilder

Gets a [builder](../concepts/builders.md) that you use to add a negative keyword list to this account. 

### Returns

|Type|Description|
|-|-
[NegativeKeywordListBuilder](./NegativeKeywordListBuilder.md)|A builder that you use to add a negative keyword list to the current account.

