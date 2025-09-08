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

| Event Type                  | Trigger Description                                                                 | Possible Statuses                          |
|------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------|
| **CARD_APPLICATION_UPDATE** | Fires when an admin approves or rejects a card application submitted using `/card/application apply` | • **SUCCESS** – Approved <br> • **FAILED** – Rejected |
| **CARD_ACTIVATION_UPDATE**  | Fires when an admin approves or rejects the card activation selfie submitted using `/card/activate`      | • **SUCCESS** – Approved <br> • **FAILED** – Rejected  |
| **CARD_LOAD_UPDATE**        | Fires when a load request submitted using `/card/topup/apply` has been rejected or loaded by an admin    | • **SUCCESS** – Loaded <br> • **FAILED** – Rejected    |
| **USER_INFO_UPDATE**        | Fires when the KYC details submitted using `/user/create` have been rejected and need to be resubmitted | • **FAILED** – Rejected                      |
| **USER_DOCUMENT_UPDATE**    | Fires when one of the documents submitted in `/user/document/upload` have been approved or rejected by an admin. If any document has been rejected, they can be resubmitted using the same API call   | • **SUCCESS** – Approved <br> • **FAILED** – Rejected |

---

## Event Types

### **CARD_APPLICATION_UPDATE**
Fires when an admin approves or rejects a card application submitted using `/card/application apply`.  

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
Fires when an admin approves or rejects the card activation selfie submitted using `/card/activate`.

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
Fires when a load request submitted using `/card/topup/apply` has been rejected or loaded by an admin.

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
Fires when the KYC details submitted using `/user/create` have been rejected and need to be resubmitted.

**Case**
- Kyc rejected

**Sample Payload**
```json
{
    "userID": "user-123",
    "status": "FAILED",
    "error": null
}
```

### **USER_DOCUMENT_UPDATE**
Fires when one of the documents submitted in `/user/document/upload` have been approved or rejected by an admin. If any document has been rejected, they can be resubmitted using the same API call.

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