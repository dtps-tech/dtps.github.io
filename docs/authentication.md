---
layout: page
title: Setup and Authentication
permalink: /setup/
nav_order: 2
---

# Setup

Need to define a **BASE_URL** variable that will hold the root URL for Merchant API in environment files.

**BASE_URL=https://sandbox.dtpspartnerapi.backofficeportal.app**

# Authentication

API authentication is the process of verifying the identity of a user that is interacting with an API.

## HMAC Authentication (Hash-based Message Authentication Code)

HMAC (Hash-based Message Authentication Code) is a mechanism that combines a cryptographic hash function with a secret key to authenticate a message's integrity and authenticity.

### Steps for HMAC Authentication

### 1. Prepare the Request Message:

Construct the request message (this could include HTTP method, request body, headers, and any query parameters). Typically, the request body, URL, HTTP method, and sometimes headers are concatenated in a specific order to form the message.

### 2. Generate the HMAC Signature:

Use a shared secret key and a cryptographic hash function (such as SHA-256) to generate the HMAC signature. The message is combined with the secret key and then hashed to create a signature.

Example to generate signature using CryptoJS -

> const signature = CryptoJS. HmacSHA256(message, secret) 
>
> CryptoJS.enc. Hex.stringify(signature)`

### 3. Send the Signature with the Request:

Include the signature in the X-Signature header (or any other header defined by the API) along with X-API-Key.

headers["X-Api-Key"] = {apiKey}  
headers["X-Api-Signature"] = {signature}
