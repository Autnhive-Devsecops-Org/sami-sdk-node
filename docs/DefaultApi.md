# DefaultApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**fileSanitization**](#filesanitization) | **POST** /ai-firewall/firewall/v1/file/sanitization | Replace content in uploaded files|
|[**multimodalChat**](#multimodalchat) | **POST** /ai-firewall/firewall/v1/prompt | Multimodal chat completions|

# **fileSanitization**
> Array<string> fileSanitization(signedUrlPayload)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    SignedUrlPayload
} from 'sami-firewall-client';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let signedUrlPayload: SignedUrlPayload; //

const { status, data } = await apiInstance.fileSanitization(
    signedUrlPayload
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **signedUrlPayload** | **SignedUrlPayload**|  | |


### Return type

**Array<string>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | file replacement results |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **multimodalChat**
> { [key: string]: any; } multimodalChat()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from 'sami-firewall-client';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let prompt: string; //Free-form prompt text (optional) (default to undefined)
let content: string; //Optional content payload (optional) (default to undefined)
let text: string; //Optional text input (optional) (default to undefined)
let input: string; //Optional input input (optional) (default to undefined)
let file: File; //Generic file upload (optional) (optional) (default to undefined)
let docx: File; //DOCX upload (optional) (optional) (default to undefined)
let pdf: File; //PDF upload (optional) (optional) (default to undefined)
let image: File; //Image upload (optional) (optional) (default to undefined)
let audio: File; //Audio upload (optional) (optional) (default to undefined)
let model: string; //Optional model name (optional) (default to undefined)

const { status, data } = await apiInstance.multimodalChat(
    prompt,
    content,
    text,
    input,
    file,
    docx,
    pdf,
    image,
    audio,
    model
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **prompt** | [**string**] | Free-form prompt text | (optional) defaults to undefined|
| **content** | [**string**] | Optional content payload | (optional) defaults to undefined|
| **text** | [**string**] | Optional text input | (optional) defaults to undefined|
| **input** | [**string**] | Optional input input | (optional) defaults to undefined|
| **file** | [**File**] | Generic file upload (optional) | (optional) defaults to undefined|
| **docx** | [**File**] | DOCX upload (optional) | (optional) defaults to undefined|
| **pdf** | [**File**] | PDF upload (optional) | (optional) defaults to undefined|
| **image** | [**File**] | Image upload (optional) | (optional) defaults to undefined|
| **audio** | [**File**] | Audio upload (optional) | (optional) defaults to undefined|
| **model** | [**string**] | Optional model name | (optional) defaults to undefined|


### Return type

**{ [key: string]: any; }**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | AI firewall chat completion response |  -  |
|**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

