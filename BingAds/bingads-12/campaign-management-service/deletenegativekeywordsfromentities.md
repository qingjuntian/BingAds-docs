---
title: DeleteNegativeKeywordsFromEntities Service Operation - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Deletes negative keywords from the specified campaign or ad group.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
> [!IMPORTANT]
> This Bing Ads API Version 12 preview documentation is subject to change. To return to version 11 content, use the version selector near the table of contents at the top and left side of the page.

# DeleteNegativeKeywordsFromEntities Service Operation - Campaign Management
Deletes negative keywords from the specified campaign or ad group.

> [!NOTE]
> The operation does not modify shared negative keyword lists.

## <a name="request"></a>Request Elements
The *DeleteNegativeKeywordsFromEntitiesRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="entitynegativekeywords"></a>EntityNegativeKeywords|An array of negative keyword with associated entity such as a campaign or ad group.<br /><br /> The *EntityType* specified within each *EntityNegativeKeyword* must be set to the same value.<br /><br />This array can contain a maximum of 1 *EntityNegativeKeyword* element, which contains up to 20,000 negative keywords.|[EntityNegativeKeyword](entitynegativekeyword.md) array|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *DeleteNegativeKeywordsFromEntitiesResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="nestedpartialerrors"></a>NestedPartialErrors|An array of [BatchErrorCollection](batcherrorcollection.md) objects that contain details for any criterion that were not successfully deleted. The top level error within each [BatchErrorCollection](batcherrorcollection.md) object corresponds to potential campaign or ad group errors. The nested list of [BatchError](batcherror.md) objects would include any errors specific to the negative keywords that you attempted to delete from the campaign or ad group.<br /><br />>The list of errors do not correspond directly to the list of items in the request. The list can be empty if there were no errors, or can include one or more error objects corresponding to each unsuccessful list item in the request.|[BatchErrorCollection](batcherrorcollection.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
The following template shows the order of the [body](#request-body) and [header](#request-header) elements for the SOAP request.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
    <Action mustUnderstand="1">DeleteNegativeKeywordsFromEntities</Action>
    <ApplicationToken i:nil="false">ValueHere</ApplicationToken>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <CustomerAccountId i:nil="false">ValueHere</CustomerAccountId>
    <CustomerId i:nil="false">ValueHere</CustomerId>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
    <Password i:nil="false">ValueHere</Password>
    <UserName i:nil="false">ValueHere</UserName>
  </s:Header>
  <s:Body>
    <DeleteNegativeKeywordsFromEntitiesRequest xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <EntityNegativeKeywords i:nil="false">
        <EntityNegativeKeyword>
          <EntityId>ValueHere</EntityId>
          <EntityType i:nil="false">ValueHere</EntityType>
          <NegativeKeywords i:nil="false">
            <NegativeKeyword>
              <Id i:nil="false">ValueHere</Id>
              <MatchType>ValueHere</MatchType>
              <Text i:nil="false">ValueHere</Text>
            </NegativeKeyword>
          </NegativeKeywords>
        </EntityNegativeKeyword>
      </EntityNegativeKeywords>
    </DeleteNegativeKeywordsFromEntitiesRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
The following template shows the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <DeleteNegativeKeywordsFromEntitiesResponse xmlns="https://bingads.microsoft.com/CampaignManagement/v12">
      <NestedPartialErrors d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <BatchErrorCollection d4p1:type="-- derived type specified here with the appropriate prefix --">
          <BatchErrors d4p1:nil="false">
            <BatchError d4p1:type="-- derived type specified here with the appropriate prefix --">
              <Code>ValueHere</Code>
              <Details d4p1:nil="false">ValueHere</Details>
              <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
              <FieldPath d4p1:nil="false">ValueHere</FieldPath>
              <ForwardCompatibilityMap xmlns:e1097="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
                <e1097:KeyValuePairOfstringstring>
                  <e1097:key d4p1:nil="false">ValueHere</e1097:key>
                  <e1097:value d4p1:nil="false">ValueHere</e1097:value>
                </e1097:KeyValuePairOfstringstring>
              </ForwardCompatibilityMap>
              <Index>ValueHere</Index>
              <Message d4p1:nil="false">ValueHere</Message>
              <Type d4p1:nil="false">ValueHere</Type>
              <!--These fields are applicable if the derived type attribute is set to EditorialError-->
              <Appealable d4p1:nil="false">ValueHere</Appealable>
              <DisapprovedText d4p1:nil="false">ValueHere</DisapprovedText>
              <Location d4p1:nil="false">ValueHere</Location>
              <PublisherCountry d4p1:nil="false">ValueHere</PublisherCountry>
              <ReasonCode>ValueHere</ReasonCode>
            </BatchError>
          </BatchErrors>
          <Code d4p1:nil="false">ValueHere</Code>
          <Details d4p1:nil="false">ValueHere</Details>
          <ErrorCode d4p1:nil="false">ValueHere</ErrorCode>
          <FieldPath d4p1:nil="false">ValueHere</FieldPath>
          <ForwardCompatibilityMap xmlns:e1098="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e1098:KeyValuePairOfstringstring>
              <e1098:key d4p1:nil="false">ValueHere</e1098:key>
              <e1098:value d4p1:nil="false">ValueHere</e1098:value>
            </e1098:KeyValuePairOfstringstring>
          </ForwardCompatibilityMap>
          <Index>ValueHere</Index>
          <Message d4p1:nil="false">ValueHere</Message>
          <Type d4p1:nil="false">ValueHere</Type>
          <!--These fields are applicable if the derived type attribute is set to EditorialErrorCollection-->
          <Appealable d4p1:nil="false">ValueHere</Appealable>
          <DisapprovedText d4p1:nil="false">ValueHere</DisapprovedText>
          <Location d4p1:nil="false">ValueHere</Location>
          <PublisherCountry d4p1:nil="false">ValueHere</PublisherCountry>
          <ReasonCode>ValueHere</ReasonCode>
        </BatchErrorCollection>
      </NestedPartialErrors>
    </DeleteNegativeKeywordsFromEntitiesResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<DeleteNegativeKeywordsFromEntitiesResponse> DeleteNegativeKeywordsFromEntitiesAsync(
	IList<EntityNegativeKeyword> entityNegativeKeywords)
{
	var request = new DeleteNegativeKeywordsFromEntitiesRequest
	{
		EntityNegativeKeywords = entityNegativeKeywords
	};

	return (await CampaignManagementService.CallAsync((s, r) => s.DeleteNegativeKeywordsFromEntitiesAsync(r), request));
}
```
```java
static DeleteNegativeKeywordsFromEntitiesResponse deleteNegativeKeywordsFromEntities(
	ArrayOfEntityNegativeKeyword entityNegativeKeywords) throws RemoteException, Exception
{
	DeleteNegativeKeywordsFromEntitiesRequest request = new DeleteNegativeKeywordsFromEntitiesRequest();

	request.setEntityNegativeKeywords(entityNegativeKeywords);

	return CampaignManagementService.getService().deleteNegativeKeywordsFromEntities(request);
}
```
```php
static function DeleteNegativeKeywordsFromEntities(
	$entityNegativeKeywords)
{

	$GLOBALS['Proxy'] = $GLOBALS['CampaignManagementProxy'];

	$request = new DeleteNegativeKeywordsFromEntitiesRequest();

	$request->EntityNegativeKeywords = $entityNegativeKeywords;

	return $GLOBALS['CampaignManagementProxy']->GetService()->DeleteNegativeKeywordsFromEntities($request);
}
```
```python
response=campaignmanagement_service.DeleteNegativeKeywordsFromEntities(
	EntityNegativeKeywords=EntityNegativeKeywords)
```

## Requirements
Service: [CampaignManagementService.svc v12](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v12/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v12  
