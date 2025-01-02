---
layout: page
title: List Topups
parent: Card Topup APIs
nav_order: 2
permalink: /api/card/topup/list/
---

# List Card Topups

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/card/topup/list?page={page}&limit={limit}

This endpoint allows you to get card topups list of a partner with pagination.

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)

Query Parameters :

| field     | type      | required  |
|:----------|:----------|:----------|
| page      | int       | yes       |
| limit     | int       | yes       |
