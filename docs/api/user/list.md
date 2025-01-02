---
layout: page
title: List Users
parent: User APIs
nav_order: 5
permalink: /api/user/list/
---

# List Users

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/user/list?page={page}&limit={limit}'

This endpoint allows you to get users list of a partner with pagination.

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)

Query Parameters :

| field     | type      | required  |
|:----------|:----------|:----------|
| page      | int       | yes       |
| limit     | int       | yes       |
