---
layout: page
title: Update User
parent: User APIs
nav_order: 3
permalink: /api/user/update/
---

# Update User

<button type="button" name="button" class="btn btn-purple fs-1">POST</button>
{BASE_URL}/api/v1/user/update/:{userID}

This endpoint allows you to update user details

{: .note}
Before proceeding with further integrations, ensure that you have set up the authentication mechanism. [Setup and Authentication](/dtps.github.io/setup)

Route Parameter :

| field     | type         | required  | source                                                                           | specifications               |
|:----------|:----------   |:----------|:---------------------------------------------------------------------------------|:-----------------------------|
| userID    | string       | yes       | id from user/create api response or specific user ID from user/list api response | unique identifier for a user |

## Body Params

[Update User Type](/dtps.github.io/types/updateUser)
