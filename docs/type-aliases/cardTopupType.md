---
layout: page
title: Card Topup Type
parent: Types
permalink: /types/cardTopup
---

# Type Alias : Card Topup

CardTopupInputDTO: object

## Type declaration

| field                | type      | required  | source                                                          | specifications                              |
|:---------------------|:----------|:----------|:----------------------------------------------------------------|:--------------------------------------------|
| userCardId           | string    | yes       | *userCardID* key from CARD_APPLICATION_UPDATE webhook response  | unique identifier for a user purchased card |
| amount               | float64   | yes       | -                                                               | needs to be 50 or greater                 |
