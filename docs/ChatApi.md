# ChatApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**adapterChat**](#adapterchat) | **POST** /ai-firewall/firewall/v1/prompt/text | Firewall text chat endpoint|

# **adapterChat**
> { [key: string]: any; } adapterChat(requestBody)


### Example

```typescript
import {
    ChatApi,
    Configuration
} from 'sami-firewall-client';

const configuration = new Configuration();
const apiInstance = new ChatApi(configuration);

let requestBody: { [key: string]: any; }; //

const { status, data } = await apiInstance.adapterChat(
    requestBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **requestBody** | **{ [key: string]: any; }**|  | |


### Return type

**{ [key: string]: any; }**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

