---
layout: page
title: Get Application By ID
parent: Card Application APIs
nav_order: 3
permalink: /api/card/applicationById
---

# Get Card Application By ID

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/card/application/:{cardApplicationId}

This endpoint allows you to get card application details by application ID.

Route Parameter :

| field             | type         | required  | source                                                                                                          | specifications               |
|:------------------|:-------------|:----------|:----------------------------------------------------------------------------------------------------------------|:---------------------------------------|
| cardApplicationId | string       | yes       | id from card/application/apply api response or specific application ID from /card/application/list api response | unique identifier for a card application|

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)
