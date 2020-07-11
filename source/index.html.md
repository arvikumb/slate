--- 

title: Enrollment Service 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

Enrollment Services will be responsible for the transfer of health insurance applications between any broker to any carrier using a standardized format. In addition, the process will maintain the data synchronization of the enrollment via status messages between the broker and carrier until such time as the application reaches the final disposition.


 

**Version:** 1.0 

# /V1/BROKER/APPLICATIONS
## ***POST*** 

**Summary:** Create Application

**Description:** Using this opeartion, a Broker can create a new Insurance Application with eHealth Enrollment Service for their carriers. 
To do this, Brokers will first need to register their platform with eHealth.

Enrollment Services authorizes and authenticates Brokers and performs schema validations to make sure Insurance Application conforms to Enrollment Services "Application" data requirements.

### HTTP Request 
`***POST*** /v1/broker/applications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/BROKER/APPLICATIONS/{BROKERAPPLICATIONID}
## ***GET*** 

**Summary:** Retrieve Application

**Description:** Broker is requesting the Application details from Enrollment Services.


### HTTP Request 
`***GET*** /v1/broker/applications/{brokerApplicationId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| timestamp | query |  | No |  |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

## ***PUT*** 

**Summary:** Update Application

**Description:** Broker is updating the Application details and sending to Enrollment Services

### HTTP Request 
`***PUT*** /v1/broker/applications/{brokerApplicationId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/BROKER/APPLICATIONS/{BROKERAPPLICATIONID}/STATUSES
## ***POST*** 

**Summary:** Create Latest Application Status

**Description:** Broker is adding a new Application Status to Enrollment Services

### HTTP Request 
`***POST*** /v1/broker/applications/{brokerApplicationId}/statuses` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

## ***GET*** 

**Summary:** Retrieve Application Statuses

**Description:** Broker is requesting the Application Status array from Enrollment Services

### HTTP Request 
`***GET*** /v1/broker/applications/{brokerApplicationId}/statuses` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/CARRIER/APPLICATIONS/{CARRIERAPPLICATIONID}/STATUSES
## ***GET*** 

**Summary:** Retrieve Application Statuses

**Description:** Carrier is requesting the Latest Carrier Application Status from Enrollment Services

### HTTP Request 
`***GET*** /v1/carrier/applications/{carrierApplicationId}/statuses` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

## ***POST*** 

**Summary:** Create Latest Application Status

**Description:** Carrier is adding a new Application Status to Enrollment Services

### HTTP Request 
`***POST*** /v1/carrier/applications/{carrierApplicationId}/statuses` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/CARRIER/APPLICATIONS/{CARRIERAPPLICATIONID}
## ***GET*** 

**Summary:** Retrieve Application

**Description:** Carrier is requesting the Application details from Enrollment Services.

### HTTP Request 
`***GET*** /v1/carrier/applications/{carrierApplicationId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

## ***PUT*** 

**Summary:** Update Application

**Description:** Carrier is updating the Application details and sending to Enrollment Services

### HTTP Request 
`***PUT*** /v1/carrier/applications/{carrierApplicationId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/EXAMPLE_CARRIER_API/APPLICATIONS
## ***POST*** 

**Summary:** Create Application

**Description:** Using this operation, provides the Carrier event to accept the Application through API

### HTTP Request 
`***POST*** /v1/example_carrier_api/applications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/BROKER/APPLICATIONS/{BROKERAPPLICATIONID}/DOCUMENTS
## ***POST*** 

**Summary:** Create Application Document

**Description:** Using this opeartion, a Broker can create a new Insurance Application Document with eHealth Enrollment Service for their carriers.

### HTTP Request 
`***POST*** /v1/broker/applications/{brokerApplicationId}/documents` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/CARRIER/APPLICATIONS/{CARRIERAPPLICATIONID}/DOCUMENTS/{DOCUMENTINDEX}
## ***GET*** 

**Summary:** Retrieve Documents

**Description:** Using this opeartion, a Carrier can request the stored documents by Carrier Application ID and Array Index.

### HTTP Request 
`***GET*** /v1/carrier/applications/{carrierApplicationId}/documents/{documentIndex}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |
| documentIndex | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/BROKER/APPLICATIONS/{BROKERAPPLICATIONID}/DOCUMENTS/{DOCUMENTINDEX}
## ***GET*** 

**Summary:** Retrieve Documents

**Description:** Using this operation, a Broker can request the stored documents by Broker Application ID and Document Array Index.

### HTTP Request 
`***GET*** /v1/broker/applications/{brokerApplicationId}/documents/{documentIndex}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |
| documentIndex | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/EXAMPLE_BROKER_API/APPLICATIONS/{BROKERAPPLICATIONID}/STATUS
## ***POST*** 

**Summary:** Create Latest Application Status

**Description:** Using this operation, provides the Broker event to accept the Application Status through API

### HTTP Request 
`***POST*** /v1/example_broker_api/applications/{brokerApplicationId}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| brokerApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

# /V1/EXAMPLE_CARRIER_API/APPLICATIONS/{CARRIERAPPLICATIONID}/STATUS
## ***POST*** 

**Summary:** Create Latest Application Status

**Description:** Using this operation, provides the Carrier event to accept the Application Status through API

### HTTP Request 
`***POST*** /v1/example_carrier_api/applications/{carrierApplicationId}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| carrierApplicationId | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 |  |
| 404 |  |
| 500 |  |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
