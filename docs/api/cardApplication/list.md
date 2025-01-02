---
layout: page
title: List Applications
parent: Card Application APIs
nav_order: 4
permalink: /api/card/application/list/
---

# List Card Applications

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/card/application/list?page={page}&limit={limit}

This endpoint allows you to get card applications list of a partner with pagination.

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)

Query Parameters :

| field     | type      | required  |
|:----------|:----------|:----------|
| page      | int       | yes       |
| limit     | int       | yes       |
