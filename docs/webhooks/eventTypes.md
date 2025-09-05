---
layout: page
title: Webhook Event Types
parent: Webhooks
permalink: /webhooks/events
---

# Webhook Event Types

Webhook events notify your system whenever important actions happen in the card or account lifecycle. Each event type corresponds to a specific update or action.  

---

## Event Summary

| Event Type                         | Trigger Description                                | Example Scenarios                                 |
|------------------------------------|----------------------------------------------------|---------------------------------------------------|
| **CARD_APPLICATION_UPDATE**        | Card application status changes                    | Application approved / rejected                   |
| **CARD_ACTIVATION_UPDATE**         | Card activation status changes                     | Activation successful / failed                    |
| **CARD_LOAD_UPDATE**               | Funds are loaded to a card account                 | Top-up approved / rejected                        |
| **USER_INFO_UPDATE**               | User profile details are updated                   | Name, email, or address updated                   |
| **USER_DOCUMENT_UPDATE**           | User uploads or updates identity documents (KYC)   | User documents approved / rejected                |
| **ONLINE_FEATURE_UPDATE**          | Online transaction features are updated            | Online transaction request approved / rejected    |
| **ONLINE_FEATURE_EXPIRY_REMINDER** | Online feature is about to expire                  | Online transcation expiring soon            |

---

## Event Types

### **CARD_APPLICATION_UPDATE**
Triggered when the status of a **card application** changes.  

**Case** 
- Application approved  
- Application rejected  

**Sample Payload**
```json
{
    "userID": "user-123",
    "applicationID": "app-456",
    "status": "SUCCESS / FAILED",
    "error": null
}
```

### **CARD_ACTIVATION_UPDATE**
Triggered when the status of a **card activation** changes.  

**Case** 
- Activated 
- Activation Rejected

**Sample Payload**
```json
{
    "userID": "user-123",
    "cardID": "card-123",
    "status": "SUCCESS / FAILED",
    "error":  "remarks",
}
```

### **CARD_LOAD_UPDATE**
Triggered when amount is **loaded to a card account**.  

**Case** 
- Card topup approved 
- Card topup rejected

**Sample Payload**
```json
{
    "userID": "user-123",
    "applicationID": "app-456",
    "status": "SUCCESS / FAILED",
    "error": null
}
```

### **USER_INFO_UPDATE**
Triggered when **user profile information** changes.

**Case** 
- User details updated 
- User update failed

**Sample Payload**
```json
{
    "userID": "user-123",
    "status": "SUCCESS / FAILED",
    "error": null
}
```

### **USER_DOCUMENT_UPDATE**
Triggered when a **user uploads or updates identity documents** (KYC).

**Case** 
- Documents updated 
- Documents update failed

**Sample Payload**
```json
{
    "userID":     "user-123",
    "documentID": "doc-123",
    "docName":    "PASSPORT / SIGNATURE / SELFIE_WITH_PASSPORT",
    "status":     "SUCCESS / FAILED",
    "error":      null,
}
```

### **ONLINE_FEATURE_UPDATE**
Triggered when **online request** is updated.

**Case** 
- Request approved 
- Request rejected

**Sample Payload**
```json
{
    "userID":  "user-123",
    "cardID":  "card-123",
    "status":  "SUCCESS / FAILED",
    "remarks": null,
}
```

### **ONLINE_FEATURE_EXPIRY_REMINDER**
Triggered when an **online request is about to expire**.

**Case** 
- Online txn request is about to expire

**Sample Payload**
```json
{
    "userID": "user-123",
    "cardID": "card-123",
}
```