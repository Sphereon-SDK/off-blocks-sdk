# FileControllerApi

All URIs are relative to *https://99.80.121.102:18080/offblocks*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auditFileByHashUsingGET**](FileControllerApi.md#auditFileByHashUsingGET) | **GET** /api/file/audit/by-hash | auditFileByHash
[**createFileUsingPOST**](FileControllerApi.md#createFileUsingPOST) | **POST** /api/file/create | createFile
[**downloadOutputFileUsingGET**](FileControllerApi.md#downloadOutputFileUsingGET) | **GET** /api/file/download/{fileId} | downloadOutputFile
[**fileSignatoryProcessUsingPOST**](FileControllerApi.md#fileSignatoryProcessUsingPOST) | **POST** /api/file/signatory | fileSignatoryProcess
[**getFileDetailsByChainIdUsingGET**](FileControllerApi.md#getFileDetailsByChainIdUsingGET) | **GET** /api/file/chain-id | getFileDetailsByChainId
[**getFileDetailsUsingGET**](FileControllerApi.md#getFileDetailsUsingGET) | **GET** /api/file | getFileDetails
[**getFileHistoryUsingGET**](FileControllerApi.md#getFileHistoryUsingGET) | **GET** /api/file/history | getFileHistory
[**getObjectChainIdUsingGET**](FileControllerApi.md#getObjectChainIdUsingGET) | **GET** /api/file/object-chain | getObjectChainId
[**getSignatureHistoryUsingGET**](FileControllerApi.md#getSignatureHistoryUsingGET) | **GET** /api/file/signature-history | getSignatureHistory
[**getUndersignedFilesUsingGET**](FileControllerApi.md#getUndersignedFilesUsingGET) | **GET** /api/file/undersigned | getUndersignedFiles
[**proveFileValidityUsingPOST**](FileControllerApi.md#proveFileValidityUsingPOST) | **POST** /api/file/proveit | proveFileValidity


<a name="auditFileByHashUsingGET"></a>
# **auditFileByHashUsingGET**
> AuditResponse auditFileByHashUsingGET(hash)

auditFileByHash

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String hash = "hash_example"; // String | hash
try {
    AuditResponse result = apiInstance.auditFileByHashUsingGET(hash);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#auditFileByHashUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hash** | **String**| hash | [optional]

### Return type

[**AuditResponse**](AuditResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

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

<a name="getFileDetailsByChainIdUsingGET"></a>
# **getFileDetailsByChainIdUsingGET**
> FileDTO getFileDetailsByChainIdUsingGET(chainId)

getFileDetailsByChainId

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String chainId = "chainId_example"; // String | chainId
try {
    FileDTO result = apiInstance.getFileDetailsByChainIdUsingGET(chainId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getFileDetailsByChainIdUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chainId** | **String**| chainId |

### Return type

[**FileDTO**](FileDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getFileDetailsUsingGET"></a>
# **getFileDetailsUsingGET**
> FileDTO getFileDetailsUsingGET(id)

getFileDetails

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    FileDTO result = apiInstance.getFileDetailsUsingGET(id);
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

[**FileDTO**](FileDTO.md)

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

<a name="getObjectChainIdUsingGET"></a>
# **getObjectChainIdUsingGET**
> String getObjectChainIdUsingGET(hash)

getObjectChainId

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String hash = "hash_example"; // String | hash
try {
    String result = apiInstance.getObjectChainIdUsingGET(hash);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getObjectChainIdUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hash** | **String**| hash |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getSignatureHistoryUsingGET"></a>
# **getSignatureHistoryUsingGET**
> List&lt;FileDetailsDTO&gt; getSignatureHistoryUsingGET(isProcessed, fileTypes, title)

getSignatureHistory

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
Boolean isProcessed = true; // Boolean | isProcessed
String fileTypes = "fileTypes_example"; // String | fileTypes
String title = "title_example"; // String | title
try {
    List<FileDetailsDTO> result = apiInstance.getSignatureHistoryUsingGET(isProcessed, fileTypes, title);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getSignatureHistoryUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **isProcessed** | **Boolean**| isProcessed |
 **fileTypes** | **String**| fileTypes | [optional]
 **title** | **String**| title | [optional]

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

<a name="proveFileValidityUsingPOST"></a>
# **proveFileValidityUsingPOST**
> Boolean proveFileValidityUsingPOST(fileRequest)

proveFileValidity

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
FileRequest fileRequest = new FileRequest(); // FileRequest | fileRequest
try {
    Boolean result = apiInstance.proveFileValidityUsingPOST(fileRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#proveFileValidityUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileRequest** | [**FileRequest**](FileRequest.md)| fileRequest |

### Return type

**Boolean**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

