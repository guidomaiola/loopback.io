---
lang: en
title: 'API docs: rest.validaterequestbody'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
permalink: /doc/en/lb4/apidocs.rest.validaterequestbody.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/rest](./rest.md) &gt; [validateRequestBody](./rest.validaterequestbody.md)

## validateRequestBody() function

Check whether the request body is valid according to the provided OpenAPI schema. The JSON schema is generated from the OpenAPI schema which is typically defined by `@requestBody()`<!-- -->. The validation leverages AJV schema validator.

<b>Signature:</b>

```typescript
export declare function validateRequestBody(body: RequestBody, requestBodySpec?: RequestBodyObject, globalSchemas?: SchemasObject, options?: RequestBodyValidationOptions): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  body | <code>RequestBody</code> | The request body parsed from an HTTP request. |
|  requestBodySpec | <code>RequestBodyObject</code> | The OpenAPI requestBody specification defined in <code>@requestBody()</code>. |
|  globalSchemas | <code>SchemasObject</code> | The referenced schemas generated from <code>OpenAPISpec.components.schemas</code>. |
|  options | <code>RequestBodyValidationOptions</code> | Request body validation options for AJV |

<b>Returns:</b>

`void`

