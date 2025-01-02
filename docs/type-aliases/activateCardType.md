---
layout: page
title: Activate Card Type
parent: Types
permalink: /types/activateCard
---

# Type Alias : Activate Card

ActivateCardInputDTO: object

## Type declaration

| field                | type      | required  | source                                                          | specifications                              |
|:---------------------|:----------|:----------|:----------------------------------------------------------------|:--------------------------------------------|
| userCardId           | string    | yes       | *userCardID* key from CARD_APPLICATION_UPDATE webhook response  | unique identifier for a user purchased card |
| selfieImg            | string    | yes       | -                                                               | image in base64 format showing the applicant holding both card and passport with information clear and readable|
