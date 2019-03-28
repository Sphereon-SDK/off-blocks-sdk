# offblocks-sdk-java8-okhttp-gson

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>com.sphereon.sdk</groupId>
    <artifactId>offblocks-sdk-java8-okhttp-gson</artifactId>
    <version>0.1-SNAPSHOT</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.sphereon.sdk:offblocks-sdk-java8-okhttp-gson:0.1-SNAPSHOT"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/offblocks-sdk-java8-okhttp-gson-0.1-SNAPSHOT.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.sphereon.sdk.offblocks.handler.*;
import com.sphereon.sdk.offblocks.handler.auth.*;
import com.sphereon.sdk.offblocks.model.*;
import com.sphereon.sdk.offblocks.api.AuthControllerApi;

import java.io.File;
import java.util.*;

public class AuthControllerApiExample {

    public static void main(String[] args) {
        
        AuthControllerApi apiInstance = new AuthControllerApi();
        LoginRequest loginRequest = new LoginRequest(); // LoginRequest | loginRequest
        try {
            Object result = apiInstance.authenticateUserUsingPOST(loginRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AuthControllerApi#authenticateUserUsingPOST");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://52.39.15.26:18080/offblocks*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthControllerApi* | [**authenticateUserUsingPOST**](docs/AuthControllerApi.md#authenticateUserUsingPOST) | **POST** /api/auth/signin | authenticateUser
*AuthControllerApi* | [**registerUserUsingPOST**](docs/AuthControllerApi.md#registerUserUsingPOST) | **POST** /api/auth/signup | registerUser
*FileControllerApi* | [**createFileUsingPOST**](docs/FileControllerApi.md#createFileUsingPOST) | **POST** /api/file/create | createFile
*FileControllerApi* | [**downloadOutputFileUsingGET**](docs/FileControllerApi.md#downloadOutputFileUsingGET) | **GET** /api/file/download/{fileId} | downloadOutputFile
*FileControllerApi* | [**fileSignatoryProcessUsingPOST**](docs/FileControllerApi.md#fileSignatoryProcessUsingPOST) | **POST** /api/file/signatory | fileSignatoryProcess
*FileControllerApi* | [**getFileDetailsUsingGET**](docs/FileControllerApi.md#getFileDetailsUsingGET) | **GET** /api/file | getFileDetails
*FileControllerApi* | [**getFileHistoryUsingGET**](docs/FileControllerApi.md#getFileHistoryUsingGET) | **GET** /api/file/history | getFileHistory
*FileControllerApi* | [**getUndersignedFilesUsingGET**](docs/FileControllerApi.md#getUndersignedFilesUsingGET) | **GET** /api/file/undersigned | getUndersignedFiles
*UserControllerApi* | [**checkEmailAvailabilityUsingGET**](docs/UserControllerApi.md#checkEmailAvailabilityUsingGET) | **GET** /api/user/checkEmailAvailability | checkEmailAvailability
*UserControllerApi* | [**checkUsernameAvailabilityUsingGET**](docs/UserControllerApi.md#checkUsernameAvailabilityUsingGET) | **GET** /api/user/checkUsernameAvailability | checkUsernameAvailability
*UserControllerApi* | [**createSignatoryListsUsingPOST**](docs/UserControllerApi.md#createSignatoryListsUsingPOST) | **POST** /api/user/signatory-list | createSignatoryLists
*UserControllerApi* | [**deleteUserUsingDELETE**](docs/UserControllerApi.md#deleteUserUsingDELETE) | **DELETE** /api/user | deleteUser
*UserControllerApi* | [**editUserUsingPUT**](docs/UserControllerApi.md#editUserUsingPUT) | **PUT** /api/user/edit | editUser
*UserControllerApi* | [**emailVerificationUsingPOST**](docs/UserControllerApi.md#emailVerificationUsingPOST) | **POST** /api/user/emailVerification | emailVerification
*UserControllerApi* | [**getCurrentUserUsingGET**](docs/UserControllerApi.md#getCurrentUserUsingGET) | **GET** /api/user/me | getCurrentUser
*UserControllerApi* | [**getSignatoryListsUsingGET**](docs/UserControllerApi.md#getSignatoryListsUsingGET) | **GET** /api/user/signatory-list | getSignatoryLists
*UserControllerApi* | [**getUserIdentityChainIdUsingGET**](docs/UserControllerApi.md#getUserIdentityChainIdUsingGET) | **GET** /api/user/chain | getUserIdentityChainId
*UserControllerApi* | [**getUserProfileUsingGET**](docs/UserControllerApi.md#getUserProfileUsingGET) | **GET** /api/users/{username} | getUserProfile
*UserControllerApi* | [**getUsersByNameOrEmailOrStaffNumberUsingGET**](docs/UserControllerApi.md#getUsersByNameOrEmailOrStaffNumberUsingGET) | **GET** /api/users | getUsersByNameOrEmailOrStaffNumber
*UserControllerApi* | [**publicKeyVerificationUsingPOST**](docs/UserControllerApi.md#publicKeyVerificationUsingPOST) | **POST** /api/user/publicKeyVerification | publicKeyVerification
*UserControllerApi* | [**userActivationUsingPOST**](docs/UserControllerApi.md#userActivationUsingPOST) | **POST** /api/user/activate | userActivation


## Documentation for Models

 - [EditUserRequest](docs/EditUserRequest.md)
 - [EmailVerificationRequest](docs/EmailVerificationRequest.md)
 - [FileDTO](docs/FileDTO.md)
 - [FileDetailsDTO](docs/FileDetailsDTO.md)
 - [FileSignatoriesDTO](docs/FileSignatoriesDTO.md)
 - [FileSignatoryDTO](docs/FileSignatoryDTO.md)
 - [InputStream](docs/InputStream.md)
 - [LoginRequest](docs/LoginRequest.md)
 - [ModelApiResponse](docs/ModelApiResponse.md)
 - [Resource](docs/Resource.md)
 - [SignUpRequest](docs/SignUpRequest.md)
 - [SignatoriesDTO](docs/SignatoriesDTO.md)
 - [SignatoryListsDTO](docs/SignatoryListsDTO.md)
 - [SignatoryListsRequest](docs/SignatoryListsRequest.md)
 - [URI](docs/URI.md)
 - [URL](docs/URL.md)
 - [UserActivationRequest](docs/UserActivationRequest.md)
 - [UserIdentityAvailability](docs/UserIdentityAvailability.md)
 - [UserProfile](docs/UserProfile.md)
 - [UserSummary](docs/UserSummary.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

myeaddress@company.com

