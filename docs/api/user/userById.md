---
layout: page
title: Get User By ID
parent: User APIs
nav_order: 4
permalink: /api/user/userbyid/
---

# Get User By ID

<button type="button" name="button" class="btn btn-purple fs-1">GET</button>
{BASE_URL}/api/v1/user/:{userID}

This endpoint allows you to get user details a partner by user ID.

Route Parameter :

| field     | type         | required  | source                                                                           | specifications               |
|:----------|:----------   |:----------|:---------------------------------------------------------------------------------|:-----------------------------|
| userID    | string       | yes       | id from user/create api response or specific user ID from user/list api response | unique identifier for a user |

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)
