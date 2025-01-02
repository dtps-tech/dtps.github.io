---
layout: page
title: Card Transaction History By CardID
parent: Card APIs
nav_order: 6
permalink: /api/card/transactionsById/
---

# Card Transaction History By CardID

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/card/txnhistory/id/:{cardId}

This endpoint allows you to get card transactions by cardId.

Route Parameter :

| field  | type      | required  | source                                                          | specifications                              |
|:-------|:----------|:----------|:----------------------------------------------------------------|:--------------------------------------------|
| cardId | string    | yes       | *userCardID* key from CARD_APPLICATION_UPDATE webhook response  | unique identifier for a user purchased card |

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)
