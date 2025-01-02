---
layout: page
title: Upload Document Type
parent: Types
permalink: /types/uploadDoc
---

# Type Alias : Upload Documents

UploadUserDocsInputDTO: object

## Type declaration

| field                | type          | required  | source                                                                           | specifications               |
|:---------------------|:--------------|:----------|:---------------------------------------------------------------------------------|:-----------------------------|
| userId               | string        | yes       | id from user/create api response or specific user ID from user/list api response | unique identifier for a user |
| documents            | []DocumentDto | yes       | -                                                                                | array of DocumentDto object  |

DocumentDto: object

| field                | type          | required  | specifications                                                       |
|:---------------------|:--------------|:----------|:---------------------------------------------------------------------|
| docName              | string        | yes       | accepted values - "PASSPORT", "SIGNATURE", "SELFIE_WITH_PASSPORT"    |
| base64data           | string        | yes       | document in base64 format                                            |

### NOTE : <br>

base64data is the image of document type PASSPORT or SIGNATURE or SELFIE_WITH_PASSPORT with below specification -

PASSPORT - Needs to show the passport biopage and ensure that all information is clear and readable

SIGNATURE - Signature specimen of the applicant. It can be a digital signature or a photo of a wet signature but do not use a typed signature where a font was used

SELFIE_WITH_PASSPORT - A clear photo of the applicant holding the passport open with the passport biopage clear and readable
