# FileControllerApi

All URIs are relative to *https://52.39.15.26:18080/offblocks*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createFileUsingPOST**](FileControllerApi.md#createFileUsingPOST) | **POST** /api/file/create | createFile
[**downloadOutputFileUsingGET**](FileControllerApi.md#downloadOutputFileUsingGET) | **GET** /api/file/download/{fileId} | downloadOutputFile
[**fileSignatoryProcessUsingPOST**](FileControllerApi.md#fileSignatoryProcessUsingPOST) | **POST** /api/file/signatory | fileSignatoryProcess
[**getFileDetailsUsingGET**](FileControllerApi.md#getFileDetailsUsingGET) | **GET** /api/file | getFileDetails
[**getFileHistoryUsingGET**](FileControllerApi.md#getFileHistoryUsingGET) | **GET** /api/file/history | getFileHistory
[**getUndersignedFilesUsingGET**](FileControllerApi.md#getUndersignedFilesUsingGET) | **GET** /api/file/undersigned | getUndersignedFiles


<a name="createFileUsingPOST"></a>
# **createFileUsingPOST**
> FileDTO createFileUsingPOST(data, file)

createFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String data = "data_example"; // String | data
File file = new File("/path/to/file.txt"); // File | file
try {
    FileDTO result = apiInstance.createFileUsingPOST(data, file);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#createFileUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | **String**| data |
 **file** | **File**| file |

### Return type

[**FileDTO**](FileDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: */*

<a name="downloadOutputFileUsingGET"></a>
# **downloadOutputFileUsingGET**
> Resource downloadOutputFileUsingGET(fileId)

downloadOutputFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String fileId = "fileId_example"; // String | fileId
try {
    Resource result = apiInstance.downloadOutputFileUsingGET(fileId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#downloadOutputFileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileId** | **String**| fileId |

### Return type

[**Resource**](Resource.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="fileSignatoryProcessUsingPOST"></a>
# **fileSignatoryProcessUsingPOST**
> List&lt;FileDetailsDTO&gt; fileSignatoryProcessUsingPOST(fileSignatoryDTO)

fileSignatoryProcess

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
FileSignatoryDTO fileSignatoryDTO = new FileSignatoryDTO(); // FileSignatoryDTO | fileSignatoryDTO
try {
    List<FileDetailsDTO> result = apiInstance.fileSignatoryProcessUsingPOST(fileSignatoryDTO);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#fileSignatoryProcessUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileSignatoryDTO** | [**FileSignatoryDTO**](FileSignatoryDTO.md)| fileSignatoryDTO |

### Return type

[**List&lt;FileDetailsDTO&gt;**](FileDetailsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="getFileDetailsUsingGET"></a>
# **getFileDetailsUsingGET**
> List&lt;FileDetailsDTO&gt; getFileDetailsUsingGET(id)

getFileDetails

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    List<FileDetailsDTO> result = apiInstance.getFileDetailsUsingGET(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getFileDetailsUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |

### Return type

[**List&lt;FileDetailsDTO&gt;**](FileDetailsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getFileHistoryUsingGET"></a>
# **getFileHistoryUsingGET**
> List&lt;FileDetailsDTO&gt; getFileHistoryUsingGET(id)

getFileHistory

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    List<FileDetailsDTO> result = apiInstance.getFileHistoryUsingGET(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getFileHistoryUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |

### Return type

[**List&lt;FileDetailsDTO&gt;**](FileDetailsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getUndersignedFilesUsingGET"></a>
# **getUndersignedFilesUsingGET**
> List&lt;FileDetailsDTO&gt; getUndersignedFilesUsingGET(isProcessed)

getUndersignedFiles

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
Boolean isProcessed = true; // Boolean | isProcessed
try {
    List<FileDetailsDTO> result = apiInstance.getUndersignedFilesUsingGET(isProcessed);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getUndersignedFilesUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **isProcessed** | **Boolean**| isProcessed |

### Return type

[**List&lt;FileDetailsDTO&gt;**](FileDetailsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

