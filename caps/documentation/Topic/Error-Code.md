---
title: Error Code
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30f9bab2-c9e1-4bbb-afa7-7c6609e39285
---
# Error Code

| Error Code | Retriable | Http Status Code | Error Message |  
|---|---|---|---|  
|internal_error | false | 500 | Unknown error occurred.|  
|request_timeout|true|408|The request is timeout. Please try again.|  
|invalid_authorization_token|false|401|The authorization token in the API request is missing.|  
|unknown_user|false|401|The user with email {userEmail} cannot be found in Content Repository.|  
|duplicated_fields_value_tuple|false|400|The values tuple &lt;{fieldsValue}&gt; of the fields tuple &lt;{fieldsName}&gt; is duplicated in the collection provided.|  
|invalid_email_value_format|false|400|The value ({emailFieldValue}) of the email ({emailField:field}) is invalid.|  
|invalid_id_value|false|400|The value ({idFieldValue}) of the id ({idField:field}) is invalid. A valid id should match the regex ^[a-zA-Z0-9-]+$.|  
|invalid_property_key_format|false|400|The property key ({propertyKey}) in properties collection is invalid. A valid property key should match the regex ^[a-zA-Z][a-zA-Z0-9_]*$.|  
|reserved_property_key|false|400|The property key ({propertyKey}) in properties collection is reserved by Content Repository and cannot be used.|  
|property_value_null|false|400|The value of the property ({propertyKey}) in properties collection is null.|  
|entity_not_found|false|400|The entity with id {entityId} and locale {entityLocale} cannot be found.|  
|entity_collection_empty|false|400|The collection of entities is null or empty.|  
|entity_field_missing|false|400|The {field:field} field of the entity is missing or empty.|  
|entity_blob_not_found|false|400|The entity blob with id {blobId} and type {blobType} under entity id {entityId} and locale {entityLocale} cannot be found.|  
|entity_blob_not_unique|false|400|The {blobType} blob type in entity type {entityType} is not defined as unique blob type.|