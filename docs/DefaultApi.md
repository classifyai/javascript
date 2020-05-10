# Classify.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewModel**](DefaultApi.md#createNewModel) | **PUT** /models | Create New Model
[**deleteModel**](DefaultApi.md#deleteModel) | **DELETE** /models | Delete Model
[**getModelsList**](DefaultApi.md#getModelsList) | **GET** /models | Get Models List
[**tagImageByUrl**](DefaultApi.md#tagImageByUrl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
[**tagLocalImage**](DefaultApi.md#tagLocalImage) | **POST** /predict | Predict by Image
[**updateModel**](DefaultApi.md#updateModel) | **POST** /models | Update Model



## createNewModel

> createNewModel(modelName)

Create New Model

Create a new custom image recognition model

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
let modelName = {"model_name":"\"Test model name\""}; // String | Set a name for your model
apiInstance.createNewModel(modelName, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **String**| Set a name for your model | 

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## deleteModel

> deleteModel(modelId)

Delete Model

Delete Model

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
let modelId = "modelId_example"; // String | You can find your model ids from Classify Dashboard.
apiInstance.deleteModel(modelId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**| You can find your model ids from Classify Dashboard. | 

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## getModelsList

> getModelsList()

Get Models List

Get the list of of models created 

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
apiInstance.getModelsList((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tagImageByUrl

> tagImageByUrl(modelId, imageUrl)

Tag Image by Using Image Url

Predict image tags by providing image url

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
let modelId = "modelId_example"; // String | Type your trained model id to predict. You get your model's id from Classify Dashboard.
let imageUrl = "imageUrl_example"; // String | Provide image url to predict
apiInstance.tagImageByUrl(modelId, imageUrl, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **imageUrl** | **String**| Provide image url to predict | 

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tagLocalImage

> tagLocalImage(modelId, opts)

Predict by Image

Send a local image to tag

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
let modelId = "modelId_example"; // String | Type your trained model id to predict. You get your model's id from Classify Dashboard.
let opts = {
  'file': "/path/to/file" // File | 
};
apiInstance.tagLocalImage(modelId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **file** | **File**|  | [optional] 

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## updateModel

> updateModel(modelName, modelId)

Update Model

Update Model Name

### Example

```javascript
import Classify from 'classify';
let defaultClient = Classify.ApiClient.instance;
// Configure API key authorization: x-api-key
let x-api-key = defaultClient.authentications['x-api-key'];
x-api-key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//x-api-key.apiKeyPrefix = 'Token';

let apiInstance = new Classify.DefaultApi();
let modelName = "modelName_example"; // String | Model Name
let modelId = "modelId_example"; // String | Model id to be renamed.
apiInstance.updateModel(modelName, modelId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **String**| Model Name | 
 **modelId** | **String**| Model id to be renamed. | 

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

