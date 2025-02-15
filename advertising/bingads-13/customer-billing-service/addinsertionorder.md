---
title: AddInsertionOrder Service Operation - Customer Billing
ms.service: bing-ads
ms.subservice: customer-billing-api
ms.topic: article
author: jonmeyers
ms.author: jonmeyers
description: Adds an insertion order to the specified account.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
# AddInsertionOrder Service Operation - Customer Billing
Adds an insertion order to the specified account.

## <a name="request"></a>Request Elements
The *AddInsertionOrderRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

> [!NOTE]
> Unless otherwise noted below, all request elements are required.

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="insertionorder"></a>InsertionOrder|An insertion order to add to the account.|[InsertionOrder](insertionorder.md)|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *AddInsertionOrderResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="createtime"></a>CreateTime|Identifies the server time in UTC when the insertion order was added.|**dateTime**|
|<a name="insertionorderid"></a>InsertionOrderId|A *long* value that represents the identifier for the insertion order that was added.|**long**|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
This template was generated by a tool to show the [order](../guides/services-protocol.md#element-order) of the [body](#request-body) and [header](#request-header) elements for the SOAP request. For supported types that you can use with this service operation, see the [Request Body Elements](#request-body) reference above.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Billing/v13">
    <Action mustUnderstand="1">AddInsertionOrder</Action>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
  </s:Header>
  <s:Body>
    <AddInsertionOrderRequest xmlns="https://bingads.microsoft.com/Billing/v13">
      <InsertionOrder xmlns:e1="https://bingads.microsoft.com/Customer/v13/Entities" i:nil="false">
        <e1:AccountId>ValueHere</e1:AccountId>
        <e1:BookingCountryCode i:nil="false">ValueHere</e1:BookingCountryCode>
        <e1:Comment i:nil="false">ValueHere</e1:Comment>
        <e1:EndDate i:nil="false">ValueHere</e1:EndDate>
        <e1:Id i:nil="false">ValueHere</e1:Id>
        <e1:LastModifiedByUserId i:nil="false">ValueHere</e1:LastModifiedByUserId>
        <e1:LastModifiedTime i:nil="false">ValueHere</e1:LastModifiedTime>
        <e1:NotificationThreshold i:nil="false">ValueHere</e1:NotificationThreshold>
        <e1:ReferenceId i:nil="false">ValueHere</e1:ReferenceId>
        <e1:SpendCapAmount i:nil="false">ValueHere</e1:SpendCapAmount>
        <e1:StartDate i:nil="false">ValueHere</e1:StartDate>
        <e1:Name i:nil="false">ValueHere</e1:Name>
        <e1:Status i:nil="false">ValueHere</e1:Status>
        <e1:PurchaseOrder i:nil="false">ValueHere</e1:PurchaseOrder>
        <e1:PendingChanges i:nil="false">
          <e1:Comment i:nil="false">ValueHere</e1:Comment>
          <e1:EndDate i:nil="false">ValueHere</e1:EndDate>
          <e1:RequestedByUserId i:nil="false">ValueHere</e1:RequestedByUserId>
          <e1:ModifiedDateTime i:nil="false">ValueHere</e1:ModifiedDateTime>
          <e1:NotificationThreshold i:nil="false">ValueHere</e1:NotificationThreshold>
          <e1:ReferenceId i:nil="false">ValueHere</e1:ReferenceId>
          <e1:SpendCapAmount i:nil="false">ValueHere</e1:SpendCapAmount>
          <e1:StartDate i:nil="false">ValueHere</e1:StartDate>
          <e1:Name i:nil="false">ValueHere</e1:Name>
          <e1:PurchaseOrder i:nil="false">ValueHere</e1:PurchaseOrder>
          <e1:ChangeStatus i:nil="false">ValueHere</e1:ChangeStatus>
        </e1:PendingChanges>
        <e1:AccountNumber i:nil="false">ValueHere</e1:AccountNumber>
        <e1:BudgetRemaining i:nil="false">ValueHere</e1:BudgetRemaining>
        <e1:BudgetSpent i:nil="false">ValueHere</e1:BudgetSpent>
        <e1:BudgetRemainingPercent i:nil="false">ValueHere</e1:BudgetRemainingPercent>
        <e1:BudgetSpentPercent i:nil="false">ValueHere</e1:BudgetSpentPercent>
        <e1:SeriesName i:nil="false">ValueHere</e1:SeriesName>
        <e1:IsInSeries i:nil="false">ValueHere</e1:IsInSeries>
        <e1:SeriesFrequencyType i:nil="false">ValueHere</e1:SeriesFrequencyType>
      </InsertionOrder>
    </AddInsertionOrderRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
This template was generated by a tool to show the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Billing/v13">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <AddInsertionOrderResponse xmlns="https://bingads.microsoft.com/Billing/v13">
      <InsertionOrderId>ValueHere</InsertionOrderId>
      <CreateTime>ValueHere</CreateTime>
    </AddInsertionOrderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads API Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<AddInsertionOrderResponse> AddInsertionOrderAsync(
	InsertionOrder insertionOrder)
{
	var request = new AddInsertionOrderRequest
	{
		InsertionOrder = insertionOrder
	};

	return (await CustomerBillingService.CallAsync((s, r) => s.AddInsertionOrderAsync(r), request));
}
```
```java
static AddInsertionOrderResponse addInsertionOrder(
	InsertionOrder insertionOrder) throws RemoteException, Exception
{
	AddInsertionOrderRequest request = new AddInsertionOrderRequest();

	request.setInsertionOrder(insertionOrder);

	return CustomerBillingService.getService().addInsertionOrder(request);
}
```
```php
static function AddInsertionOrder(
	$insertionOrder)
{

	$GLOBALS['Proxy'] = $GLOBALS['CustomerBillingProxy'];

	$request = new AddInsertionOrderRequest();

	$request->InsertionOrder = $insertionOrder;

	return $GLOBALS['CustomerBillingProxy']->GetService()->AddInsertionOrder($request);
}
```
```python
response=customerbilling_service.AddInsertionOrder(
	InsertionOrder=InsertionOrder)
```

## Requirements
Service: [CustomerBillingService.svc v13](https://clientcenter.api.bingads.microsoft.com/Api/Billing/v13/CustomerBillingService.svc)  
Namespace: https\://bingads.microsoft.com/Billing/v13  

