---
title: GetCustomer Service Operation - Customer Management
ms.service: bing-ads
ms.subservice: customer-management-api
ms.topic: article
author: jonmeyers
ms.author: jonmeyers
description: Gets the details of a customer.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
# GetCustomer Service Operation - Customer Management
Gets the details of a customer.

## <a name="request"></a>Request Elements
The *GetCustomerRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

> [!NOTE]
> Unless otherwise noted below, all request elements are required.

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="customerid"></a>CustomerId|The identifier of the customer whose information you want to get.|**long**|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *GetCustomerResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="customer"></a>Customer|A *Customer* object that contains information about the customer.|[Customer](customer.md)|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
This template was generated by a tool to show the [order](../guides/services-protocol.md#element-order) of the [body](#request-body) and [header](#request-header) elements for the SOAP request. For supported types that you can use with this service operation, see the [Request Body Elements](#request-body) reference above.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v13">
    <Action mustUnderstand="1">GetCustomer</Action>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
  </s:Header>
  <s:Body>
    <GetCustomerRequest xmlns="https://bingads.microsoft.com/Customer/v13">
      <CustomerId>ValueHere</CustomerId>
    </GetCustomerRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
This template was generated by a tool to show the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v13">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <GetCustomerResponse xmlns="https://bingads.microsoft.com/Customer/v13">
      <Customer xmlns:e217="https://bingads.microsoft.com/Customer/v13/Entities" d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <e217:CustomerFinancialStatus d4p1:nil="false">ValueHere</e217:CustomerFinancialStatus>
        <e217:Id d4p1:nil="false">ValueHere</e217:Id>
        <e217:Industry d4p1:nil="false">ValueHere</e217:Industry>
        <e217:LastModifiedByUserId d4p1:nil="false">ValueHere</e217:LastModifiedByUserId>
        <e217:LastModifiedTime d4p1:nil="false">ValueHere</e217:LastModifiedTime>
        <e217:MarketCountry d4p1:nil="false">ValueHere</e217:MarketCountry>
        <e217:ForwardCompatibilityMap xmlns:e218="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
          <e218:KeyValuePairOfstringstring>
            <e218:key d4p1:nil="false">ValueHere</e218:key>
            <e218:value d4p1:nil="false">ValueHere</e218:value>
          </e218:KeyValuePairOfstringstring>
        </e217:ForwardCompatibilityMap>
        <e217:MarketLanguage d4p1:nil="false">ValueHere</e217:MarketLanguage>
        <e217:Name d4p1:nil="false">ValueHere</e217:Name>
        <e217:ServiceLevel d4p1:nil="false">ValueHere</e217:ServiceLevel>
        <e217:CustomerLifeCycleStatus d4p1:nil="false">ValueHere</e217:CustomerLifeCycleStatus>
        <e217:TimeStamp d4p1:nil="false">ValueHere</e217:TimeStamp>
        <e217:Number d4p1:nil="false">ValueHere</e217:Number>
        <e217:CustomerAddress d4p1:nil="false">
          <e217:City d4p1:nil="false">ValueHere</e217:City>
          <e217:CountryCode d4p1:nil="false">ValueHere</e217:CountryCode>
          <e217:Id d4p1:nil="false">ValueHere</e217:Id>
          <e217:Line1 d4p1:nil="false">ValueHere</e217:Line1>
          <e217:Line2 d4p1:nil="false">ValueHere</e217:Line2>
          <e217:Line3 d4p1:nil="false">ValueHere</e217:Line3>
          <e217:Line4 d4p1:nil="false">ValueHere</e217:Line4>
          <e217:PostalCode d4p1:nil="false">ValueHere</e217:PostalCode>
          <e217:StateOrProvince d4p1:nil="false">ValueHere</e217:StateOrProvince>
          <e217:TimeStamp d4p1:nil="false">ValueHere</e217:TimeStamp>
          <e217:BusinessName d4p1:nil="false">ValueHere</e217:BusinessName>
        </e217:CustomerAddress>
      </Customer>
    </GetCustomerResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads API Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<GetCustomerResponse> GetCustomerAsync(
	long customerId)
{
	var request = new GetCustomerRequest
	{
		CustomerId = customerId
	};

	return (await CustomerManagementService.CallAsync((s, r) => s.GetCustomerAsync(r), request));
}
```
```java
static GetCustomerResponse getCustomer(
	java.lang.Long customerId) throws RemoteException, Exception
{
	GetCustomerRequest request = new GetCustomerRequest();

	request.setCustomerId(customerId);

	return CustomerManagementService.getService().getCustomer(request);
}
```
```php
static function GetCustomer(
	$customerId)
{

	$GLOBALS['Proxy'] = $GLOBALS['CustomerManagementProxy'];

	$request = new GetCustomerRequest();

	$request->CustomerId = $customerId;

	return $GLOBALS['CustomerManagementProxy']->GetService()->GetCustomer($request);
}
```
```python
response=customermanagement_service.GetCustomer(
	CustomerId=CustomerId)
```

## Requirements
Service: [CustomerManagementService.svc v13](https://clientcenter.api.bingads.microsoft.com/Api/CustomerManagement/v13/CustomerManagementService.svc)  
Namespace: https\://bingads.microsoft.com/Customer/v13  

