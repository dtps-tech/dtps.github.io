---
layout: page
title: Apply Card Type
parent: Types
permalink: /types/applyCard
---

# Type Alias : Apply Card

ApplyCardInputDTO: object

## Type declaration

| field                | type      | required  | source                                                                           | specifications               |
|:---------------------|:----------|:----------|:---------------------------------------------------------------------------------|:-----------------------------|
| userId               | string    | yes       | id from user/create api response or specific user ID from user/list api response | unique identifier for a user |
| cardId               | string    | yes       | specific card ID from card/list api response                                     | unique identifier for a card |
| embossname           | string    | yes       | -                                                                                | Name to be printed on the front of the card. This needs to use the Latin alphabet and should not contain any special characters. Maximum characters is 21.|
| carddeliveryaddress  | string    | yes       | -                                                                                | Please provide the full address of the applicant in a similar format, (e.g: Street address, town, city, state, country, postal code)                            |
| accountNumber        | string    | optional  | -                                                                                | exactly 17 digits            |
| cardNumber           | string    | optional  | -                                                                                | exactly 16 digits            |
