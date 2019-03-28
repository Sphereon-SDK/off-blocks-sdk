# AuthControllerApi

All URIs are relative to *https://52.39.15.26:18080/offblocks*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authenticateUserUsingPOST**](AuthControllerApi.md#authenticateUserUsingPOST) | **POST** /api/auth/signin | authenticateUser
[**registerUserUsingPOST**](AuthControllerApi.md#registerUserUsingPOST) | **POST** /api/auth/signup | registerUser


<a name="authenticateUserUsingPOST"></a>
# **authenticateUserUsingPOST**
> Object authenticateUserUsingPOST(loginRequest)

authenticateUser

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.AuthControllerApi;


AuthControllerApi apiInstance = new AuthControllerApi();
LoginRequest loginRequest = new LoginRequest(); // LoginRequest | loginRequest
try {
    Object result = apiInstance.authenticateUserUsingPOST(loginRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling AuthControllerApi#authenticateUserUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **loginRequest** | [**LoginRequest**](LoginRequest.md)| loginRequest |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="registerUserUsingPOST"></a>
# **registerUserUsingPOST**
> Object registerUserUsingPOST(signUpRequest)

registerUser

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.AuthControllerApi;


AuthControllerApi apiInstance = new AuthControllerApi();
SignUpRequest signUpRequest = new SignUpRequest(); // SignUpRequest | signUpRequest
try {
    Object result = apiInstance.registerUserUsingPOST(signUpRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling AuthControllerApi#registerUserUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signUpRequest** | [**SignUpRequest**](SignUpRequest.md)| signUpRequest |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

