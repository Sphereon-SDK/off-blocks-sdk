# UserControllerApi

All URIs are relative to *https://52.39.15.26:18080/offblocks*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addContactUsingPOST**](UserControllerApi.md#addContactUsingPOST) | **POST** /api/user/contact | addContact
[**checkEmailAvailabilityUsingGET**](UserControllerApi.md#checkEmailAvailabilityUsingGET) | **GET** /api/user/checkEmailAvailability | checkEmailAvailability
[**checkUsernameAvailabilityUsingGET**](UserControllerApi.md#checkUsernameAvailabilityUsingGET) | **GET** /api/user/checkUsernameAvailability | checkUsernameAvailability
[**createSignatoryListsUsingPOST**](UserControllerApi.md#createSignatoryListsUsingPOST) | **POST** /api/user/signatory-list | createSignatoryLists
[**deleteContactUsingDELETE**](UserControllerApi.md#deleteContactUsingDELETE) | **DELETE** /api/user/contact | deleteContact
[**deleteSignatoryListUsingDELETE**](UserControllerApi.md#deleteSignatoryListUsingDELETE) | **DELETE** /api/user/signatory-list | deleteSignatoryList
[**deleteUserUsingDELETE**](UserControllerApi.md#deleteUserUsingDELETE) | **DELETE** /api/user | deleteUser
[**editUserUsingPUT**](UserControllerApi.md#editUserUsingPUT) | **PUT** /api/user/edit | editUser
[**emailVerificationUsingPOST**](UserControllerApi.md#emailVerificationUsingPOST) | **POST** /api/user/emailVerification | emailVerification
[**getContactsUsingGET**](UserControllerApi.md#getContactsUsingGET) | **GET** /api/user/contacts | getContacts
[**getCurrentUserUsingGET**](UserControllerApi.md#getCurrentUserUsingGET) | **GET** /api/user/me | getCurrentUser
[**getSignatoryListsUsingGET**](UserControllerApi.md#getSignatoryListsUsingGET) | **GET** /api/user/signatory-list | getSignatoryLists
[**getUserIdentityChainIdUsingGET**](UserControllerApi.md#getUserIdentityChainIdUsingGET) | **GET** /api/user/chain | getUserIdentityChainId
[**getUserProfileUsingGET**](UserControllerApi.md#getUserProfileUsingGET) | **GET** /api/users/{username} | getUserProfile
[**getUsersByNameOrEmailOrStaffNumberUsingGET**](UserControllerApi.md#getUsersByNameOrEmailOrStaffNumberUsingGET) | **GET** /api/users | getUsersByNameOrEmailOrStaffNumber
[**publicKeyVerificationUsingPOST**](UserControllerApi.md#publicKeyVerificationUsingPOST) | **POST** /api/user/publicKeyVerification | publicKeyVerification
[**userActivationUsingPOST**](UserControllerApi.md#userActivationUsingPOST) | **POST** /api/user/activate | userActivation


<a name="addContactUsingPOST"></a>
# **addContactUsingPOST**
> UserProfile addContactUsingPOST(editUserRequest)

addContact

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
EditUserRequest editUserRequest = new EditUserRequest(); // EditUserRequest | editUserRequest
try {
    UserProfile result = apiInstance.addContactUsingPOST(editUserRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#addContactUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **editUserRequest** | [**EditUserRequest**](EditUserRequest.md)| editUserRequest |

### Return type

[**UserProfile**](UserProfile.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="checkEmailAvailabilityUsingGET"></a>
# **checkEmailAvailabilityUsingGET**
> UserIdentityAvailability checkEmailAvailabilityUsingGET(email)

checkEmailAvailability

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String email = "email_example"; // String | email
try {
    UserIdentityAvailability result = apiInstance.checkEmailAvailabilityUsingGET(email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#checkEmailAvailabilityUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| email |

### Return type

[**UserIdentityAvailability**](UserIdentityAvailability.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="checkUsernameAvailabilityUsingGET"></a>
# **checkUsernameAvailabilityUsingGET**
> UserIdentityAvailability checkUsernameAvailabilityUsingGET(username)

checkUsernameAvailability

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String username = "username_example"; // String | username
try {
    UserIdentityAvailability result = apiInstance.checkUsernameAvailabilityUsingGET(username);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#checkUsernameAvailabilityUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| username |

### Return type

[**UserIdentityAvailability**](UserIdentityAvailability.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="createSignatoryListsUsingPOST"></a>
# **createSignatoryListsUsingPOST**
> SignatoryListsDTO createSignatoryListsUsingPOST(signatoryListsRequest)

createSignatoryLists

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
SignatoryListsRequest signatoryListsRequest = new SignatoryListsRequest(); // SignatoryListsRequest | signatoryListsRequest
try {
    SignatoryListsDTO result = apiInstance.createSignatoryListsUsingPOST(signatoryListsRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#createSignatoryListsUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signatoryListsRequest** | [**SignatoryListsRequest**](SignatoryListsRequest.md)| signatoryListsRequest |

### Return type

[**SignatoryListsDTO**](SignatoryListsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="deleteContactUsingDELETE"></a>
# **deleteContactUsingDELETE**
> ModelApiResponse deleteContactUsingDELETE(userId)

deleteContact

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String userId = "userId_example"; // String | userId
try {
    ModelApiResponse result = apiInstance.deleteContactUsingDELETE(userId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#deleteContactUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| userId |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="deleteSignatoryListUsingDELETE"></a>
# **deleteSignatoryListUsingDELETE**
> ModelApiResponse deleteSignatoryListUsingDELETE(signatoryListId)

deleteSignatoryList

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String signatoryListId = "signatoryListId_example"; // String | signatoryListId
try {
    ModelApiResponse result = apiInstance.deleteSignatoryListUsingDELETE(signatoryListId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#deleteSignatoryListUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signatoryListId** | **String**| signatoryListId |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="deleteUserUsingDELETE"></a>
# **deleteUserUsingDELETE**
> Object deleteUserUsingDELETE()

deleteUser

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
try {
    Object result = apiInstance.deleteUserUsingDELETE();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#deleteUserUsingDELETE");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="editUserUsingPUT"></a>
# **editUserUsingPUT**
> Object editUserUsingPUT(editUserRequest)

editUser

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
EditUserRequest editUserRequest = new EditUserRequest(); // EditUserRequest | editUserRequest
try {
    Object result = apiInstance.editUserUsingPUT(editUserRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#editUserUsingPUT");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **editUserRequest** | [**EditUserRequest**](EditUserRequest.md)| editUserRequest |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="emailVerificationUsingPOST"></a>
# **emailVerificationUsingPOST**
> UserIdentityAvailability emailVerificationUsingPOST(emailVerificationRequest)

emailVerification

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
EmailVerificationRequest emailVerificationRequest = new EmailVerificationRequest(); // EmailVerificationRequest | emailVerificationRequest
try {
    UserIdentityAvailability result = apiInstance.emailVerificationUsingPOST(emailVerificationRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#emailVerificationUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailVerificationRequest** | [**EmailVerificationRequest**](EmailVerificationRequest.md)| emailVerificationRequest |

### Return type

[**UserIdentityAvailability**](UserIdentityAvailability.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="getContactsUsingGET"></a>
# **getContactsUsingGET**
> List&lt;UserProfile&gt; getContactsUsingGET()

getContacts

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
try {
    List<UserProfile> result = apiInstance.getContactsUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getContactsUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;UserProfile&gt;**](UserProfile.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getCurrentUserUsingGET"></a>
# **getCurrentUserUsingGET**
> UserSummary getCurrentUserUsingGET(accountNonExpired, accountNonLocked, authorities0Authority, business, credentialsNonExpired, email, enabled, id, joinedAt, lastName, name, password, username)

getCurrentUser

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
Boolean accountNonExpired = true; // Boolean | 
Boolean accountNonLocked = true; // Boolean | 
String authorities0Authority = "authorities0Authority_example"; // String | 
Boolean business = true; // Boolean | 
Boolean credentialsNonExpired = true; // Boolean | 
String email = "email_example"; // String | 
Boolean enabled = true; // Boolean | 
String id = "id_example"; // String | 
OffsetDateTime joinedAt = new OffsetDateTime(); // OffsetDateTime | 
String lastName = "lastName_example"; // String | 
String name = "name_example"; // String | 
String password = "password_example"; // String | 
String username = "username_example"; // String | 
try {
    UserSummary result = apiInstance.getCurrentUserUsingGET(accountNonExpired, accountNonLocked, authorities0Authority, business, credentialsNonExpired, email, enabled, id, joinedAt, lastName, name, password, username);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getCurrentUserUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountNonExpired** | **Boolean**|  | [optional]
 **accountNonLocked** | **Boolean**|  | [optional]
 **authorities0Authority** | **String**|  | [optional]
 **business** | **Boolean**|  | [optional]
 **credentialsNonExpired** | **Boolean**|  | [optional]
 **email** | **String**|  | [optional]
 **enabled** | **Boolean**|  | [optional]
 **id** | **String**|  | [optional]
 **joinedAt** | **OffsetDateTime**|  | [optional]
 **lastName** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **password** | **String**|  | [optional]
 **username** | **String**|  | [optional]

### Return type

[**UserSummary**](UserSummary.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getSignatoryListsUsingGET"></a>
# **getSignatoryListsUsingGET**
> List&lt;SignatoryListsDTO&gt; getSignatoryListsUsingGET()

getSignatoryLists

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
try {
    List<SignatoryListsDTO> result = apiInstance.getSignatoryListsUsingGET();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getSignatoryListsUsingGET");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;SignatoryListsDTO&gt;**](SignatoryListsDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getUserIdentityChainIdUsingGET"></a>
# **getUserIdentityChainIdUsingGET**
> ModelApiResponse getUserIdentityChainIdUsingGET(userId)

getUserIdentityChainId

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String userId = "userId_example"; // String | userId
try {
    ModelApiResponse result = apiInstance.getUserIdentityChainIdUsingGET(userId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getUserIdentityChainIdUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| userId |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getUserProfileUsingGET"></a>
# **getUserProfileUsingGET**
> UserProfile getUserProfileUsingGET(username)

getUserProfile

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String username = "username_example"; // String | username
try {
    UserProfile result = apiInstance.getUserProfileUsingGET(username);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getUserProfileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**| username |

### Return type

[**UserProfile**](UserProfile.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="getUsersByNameOrEmailOrStaffNumberUsingGET"></a>
# **getUsersByNameOrEmailOrStaffNumberUsingGET**
> List&lt;UserProfile&gt; getUsersByNameOrEmailOrStaffNumberUsingGET(search)

getUsersByNameOrEmailOrStaffNumber

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
String search = "search_example"; // String | search
try {
    List<UserProfile> result = apiInstance.getUsersByNameOrEmailOrStaffNumberUsingGET(search);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#getUsersByNameOrEmailOrStaffNumberUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | **String**| search |

### Return type

[**List&lt;UserProfile&gt;**](UserProfile.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

<a name="publicKeyVerificationUsingPOST"></a>
# **publicKeyVerificationUsingPOST**
> UserIdentityAvailability publicKeyVerificationUsingPOST(userActivationRequest)

publicKeyVerification

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
UserActivationRequest userActivationRequest = new UserActivationRequest(); // UserActivationRequest | userActivationRequest
try {
    UserIdentityAvailability result = apiInstance.publicKeyVerificationUsingPOST(userActivationRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#publicKeyVerificationUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userActivationRequest** | [**UserActivationRequest**](UserActivationRequest.md)| userActivationRequest |

### Return type

[**UserIdentityAvailability**](UserIdentityAvailability.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="userActivationUsingPOST"></a>
# **userActivationUsingPOST**
> ModelApiResponse userActivationUsingPOST(userActivationRequest)

userActivation

### Example
```java
// Import classes:
//import com.sphereon.sdk.offblocks.handler.ApiException;
//import com.sphereon.sdk.offblocks.api.UserControllerApi;


UserControllerApi apiInstance = new UserControllerApi();
UserActivationRequest userActivationRequest = new UserActivationRequest(); // UserActivationRequest | userActivationRequest
try {
    ModelApiResponse result = apiInstance.userActivationUsingPOST(userActivationRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserControllerApi#userActivationUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userActivationRequest** | [**UserActivationRequest**](UserActivationRequest.md)| userActivationRequest |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

