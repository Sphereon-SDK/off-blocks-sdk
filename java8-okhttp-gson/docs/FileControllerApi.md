# FileControllerApi

All URIs are relative to *https://api.acc.off-blocks.com/offblocks*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auditFileByHashUsingGET**](FileControllerApi.md#auditFileByHashUsingGET) | **GET** /api/file/audit/by-hash | auditFileByHash
[**createFileTemplateUsingPOST**](FileControllerApi.md#createFileTemplateUsingPOST) | **POST** /api/file/create-template | createFileTemplate
[**createFileUsingPOST**](FileControllerApi.md#createFileUsingPOST) | **POST** /api/file/create | createFile
[**deleteFileUsingDELETE**](FileControllerApi.md#deleteFileUsingDELETE) | **DELETE** /api/file | deleteFile
[**deleteTemplateUsingDELETE**](FileControllerApi.md#deleteTemplateUsingDELETE) | **DELETE** /api/file/template | deleteTemplate
[**downloadManagedOutputFileUsingGET**](FileControllerApi.md#downloadManagedOutputFileUsingGET) | **GET** /api/file/managed/download/{managedUserSignUuid} | downloadManagedOutputFile
[**downloadOutputFileUsingGET**](FileControllerApi.md#downloadOutputFileUsingGET) | **GET** /api/file/download/{fileId} | downloadOutputFile
[**downloadOutputSignatoryFileUsingGET**](FileControllerApi.md#downloadOutputSignatoryFileUsingGET) | **GET** /api/file/download-signatories/{annotatedFileId} | downloadOutputSignatoryFile
[**downloadOutputTemplateFileUsingGET**](FileControllerApi.md#downloadOutputTemplateFileUsingGET) | **GET** /api/file/download-template/{templateId} | downloadOutputTemplateFile
[**getFileDetailsByChainIdUsingGET**](FileControllerApi.md#getFileDetailsByChainIdUsingGET) | **GET** /api/file/chain-id | getFileDetailsByChainId
[**getFileDetailsUsingGET**](FileControllerApi.md#getFileDetailsUsingGET) | **GET** /api/file | getFileDetails
[**getFileHistoryUsingGET**](FileControllerApi.md#getFileHistoryUsingGET) | **GET** /api/file/history | getFileHistory
[**getGeneralFileStatusStatisticsUsingGET**](FileControllerApi.md#getGeneralFileStatusStatisticsUsingGET) | **GET** /api/file/file-statistics | getGeneralFileStatusStatistics
[**getManagedFileDetailsUsingGET**](FileControllerApi.md#getManagedFileDetailsUsingGET) | **GET** /api/file/managed | getManagedFileDetails
[**getObjectChainIdUsingGET**](FileControllerApi.md#getObjectChainIdUsingGET) | **GET** /api/file/object-chain | getObjectChainId
[**getSignatureHistoryUsingGET**](FileControllerApi.md#getSignatureHistoryUsingGET) | **GET** /api/file/signature-history | getSignatureHistory
[**getUndersignedFilesUsingGET**](FileControllerApi.md#getUndersignedFilesUsingGET) | **GET** /api/file/undersigned | getUndersignedFiles
[**getUserFilesUsingGET**](FileControllerApi.md#getUserFilesUsingGET) | **GET** /api/file/files | getUserFiles
[**getUserTemplatesUsingGET**](FileControllerApi.md#getUserTemplatesUsingGET) | **GET** /api/file/templates | getUserTemplates
[**proveFileUsingGET**](FileControllerApi.md#proveFileUsingGET) | **GET** /api/file/prove | proveFile
[**proveFileValidityUsingPOST**](FileControllerApi.md#proveFileValidityUsingPOST) | **POST** /api/file/proveit | proveFileValidity
[**proveOutputFileUsingGET**](FileControllerApi.md#proveOutputFileUsingGET) | **GET** /api/file/prove/{fileId} | proveOutputFile
[**recoverRejectedFileUsingPOST**](FileControllerApi.md#recoverRejectedFileUsingPOST) | **POST** /api/file/sign-recovery | recoverRejectedFile
[**updateFileSigningExpiryUsingGET**](FileControllerApi.md#updateFileSigningExpiryUsingGET) | **GET** /api/file/signing-expiry | updateFileSigningExpiry


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
 **hash** | **String**| hash |

### Return type

[**AuditResponse**](AuditResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="createFileTemplateUsingPOST"></a>
# **createFileTemplateUsingPOST**
> FileDTO createFileTemplateUsingPOST(data, file)

createFileTemplate

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String data = "data_example"; // String | data
File file = new File("/path/to/file.txt"); // File | file
try {
    FileDTO result = apiInstance.createFileTemplateUsingPOST(data, file);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#createFileTemplateUsingPOST");
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

<a name="createFileUsingPOST"></a>
# **createFileUsingPOST**
> FileDTO createFileUsingPOST(data, file)

createFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiClient;
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.handler.Configuration;
//import com.sphereon.sdk.offblocks.handler.auth.*;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: oauth2schema
OAuth oauth2schema = (OAuth) defaultClient.getAuthentication("oauth2schema");
oauth2schema.setAccessToken("YOUR ACCESS TOKEN");

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

[oauth2schema](../README.md#oauth2schema)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: */*

<a name="deleteFileUsingDELETE"></a>
# **deleteFileUsingDELETE**
> Object deleteFileUsingDELETE(id)

deleteFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    Object result = apiInstance.deleteFileUsingDELETE(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#deleteFileUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="deleteTemplateUsingDELETE"></a>
# **deleteTemplateUsingDELETE**
> Object deleteTemplateUsingDELETE(id)

deleteTemplate

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    Object result = apiInstance.deleteTemplateUsingDELETE(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#deleteTemplateUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="downloadManagedOutputFileUsingGET"></a>
# **downloadManagedOutputFileUsingGET**
> Resource downloadManagedOutputFileUsingGET(managedUserSignUuid)

downloadManagedOutputFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String managedUserSignUuid = "managedUserSignUuid_example"; // String | managedUserSignUuid
try {
    Resource result = apiInstance.downloadManagedOutputFileUsingGET(managedUserSignUuid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#downloadManagedOutputFileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **managedUserSignUuid** | **String**| managedUserSignUuid |

### Return type

[**Resource**](Resource.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
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

<a name="downloadOutputSignatoryFileUsingGET"></a>
# **downloadOutputSignatoryFileUsingGET**
> Resource downloadOutputSignatoryFileUsingGET(annotatedFileId)

downloadOutputSignatoryFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String annotatedFileId = "annotatedFileId_example"; // String | annotatedFileId
try {
    Resource result = apiInstance.downloadOutputSignatoryFileUsingGET(annotatedFileId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#downloadOutputSignatoryFileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotatedFileId** | **String**| annotatedFileId |

### Return type

[**Resource**](Resource.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="downloadOutputTemplateFileUsingGET"></a>
# **downloadOutputTemplateFileUsingGET**
> Resource downloadOutputTemplateFileUsingGET(templateId)

downloadOutputTemplateFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String templateId = "templateId_example"; // String | templateId
try {
    Resource result = apiInstance.downloadOutputTemplateFileUsingGET(templateId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#downloadOutputTemplateFileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | **String**| templateId |

### Return type

[**Resource**](Resource.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
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

<a name="getGeneralFileStatusStatisticsUsingGET"></a>
# **getGeneralFileStatusStatisticsUsingGET**
> FileStatisticsDTO getGeneralFileStatusStatisticsUsingGET()

getGeneralFileStatusStatistics

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
try {
    FileStatisticsDTO result = apiInstance.getGeneralFileStatusStatisticsUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getGeneralFileStatusStatisticsUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FileStatisticsDTO**](FileStatisticsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getManagedFileDetailsUsingGET"></a>
# **getManagedFileDetailsUsingGET**
> FileDTO getManagedFileDetailsUsingGET(id)

getManagedFileDetails

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String id = "id_example"; // String | id
try {
    FileDTO result = apiInstance.getManagedFileDetailsUsingGET(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getManagedFileDetailsUsingGET");
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
> List&lt;FileDetailsDTO&gt; getSignatureHistoryUsingGET(isProcessed, blockchainEventRole, fileTypes, inProgress, isCreator, title)

getSignatureHistory

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
Boolean isProcessed = true; // Boolean | isProcessed
List<String> blockchainEventRole = Arrays.asList("blockchainEventRole_example"); // List<String> | blockchainEventRole
List<String> fileTypes = Arrays.asList("fileTypes_example"); // List<String> | fileTypes
Boolean inProgress = false; // Boolean | inProgress
Boolean isCreator = false; // Boolean | isCreator
String title = "title_example"; // String | title
try {
    List<FileDetailsDTO> result = apiInstance.getSignatureHistoryUsingGET(isProcessed, blockchainEventRole, fileTypes, inProgress, isCreator, title);
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
 **blockchainEventRole** | [**List&lt;String&gt;**](String.md)| blockchainEventRole | [optional]
 **fileTypes** | [**List&lt;String&gt;**](String.md)| fileTypes | [optional]
 **inProgress** | **Boolean**| inProgress | [optional] [default to false]
 **isCreator** | **Boolean**| isCreator | [optional] [default to false]
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

<a name="getUserFilesUsingGET"></a>
# **getUserFilesUsingGET**
> List&lt;FileDTO&gt; getUserFilesUsingGET()

getUserFiles

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
try {
    List<FileDTO> result = apiInstance.getUserFilesUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getUserFilesUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;FileDTO&gt;**](FileDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getUserTemplatesUsingGET"></a>
# **getUserTemplatesUsingGET**
> List&lt;FileDTO&gt; getUserTemplatesUsingGET()

getUserTemplates

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
try {
    List<FileDTO> result = apiInstance.getUserTemplatesUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#getUserTemplatesUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;FileDTO&gt;**](FileDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="proveFileUsingGET"></a>
# **proveFileUsingGET**
> Boolean proveFileUsingGET()

proveFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
try {
    Boolean result = apiInstance.proveFileUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#proveFileUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**Boolean**

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

<a name="proveOutputFileUsingGET"></a>
# **proveOutputFileUsingGET**
> Resource proveOutputFileUsingGET(fileId)

proveOutputFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
String fileId = "fileId_example"; // String | fileId
try {
    Resource result = apiInstance.proveOutputFileUsingGET(fileId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#proveOutputFileUsingGET");
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

<a name="recoverRejectedFileUsingPOST"></a>
# **recoverRejectedFileUsingPOST**
> recoverRejectedFileUsingPOST(fileRequest)

recoverRejectedFile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
FileRequest fileRequest = new FileRequest(); // FileRequest | fileRequest
try {
    apiInstance.recoverRejectedFileUsingPOST(fileRequest);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#recoverRejectedFileUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileRequest** | [**FileRequest**](FileRequest.md)| fileRequest |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="updateFileSigningExpiryUsingGET"></a>
# **updateFileSigningExpiryUsingGET**
> Boolean updateFileSigningExpiryUsingGET()

updateFileSigningExpiry

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.FileControllerApi;


FileControllerApi apiInstance = new FileControllerApi();
try {
    Boolean result = apiInstance.updateFileSigningExpiryUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling FileControllerApi#updateFileSigningExpiryUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**Boolean**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

