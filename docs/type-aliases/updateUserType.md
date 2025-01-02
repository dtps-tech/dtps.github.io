---
layout: page
title: Update User Type
parent: Types
permalink: /types/updateUser
---

# Type Alias : Update User

UpdateUserInputDTO: object

## Type declaration

| field                | type      | required  | specifications                              |
|:---------------------|:----------|:----------|:--------------------------------------------|
| title                | string    | optional  | maximum 5 characters eg: Mr, Ms, Dr         |
| first_name           | string    | yes       | Only use Latin alphabet. Must be exact name as SHOWN on passport; otherwise the application may be rejected. If the passport name has any special characters, please transliterate to the Latin alphabet |
| last_name            | string    | yes       | Only use Latin alphabet. Must be exact last name as SHOWN on passport; otherwise the application may be rejected. If the passport name has any special characters, please transliterate to the Latin alphabet|
| gender               | string    | optional  | accepted values - Male, Female, Other, None |
| dob                  | string    | optional  | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
| place_of_birth       | string    | optional  | full country name, maximum 50 characters    |
| birth_country        | string    | optional  | 2-digit ISO format eg: Australia = AU       |
| village              | string    | optional  | Equivalent to the applicant's current street address. This needs to connect with the other parameters "district" and "province |
| district             | string    | optional  | Equivalent to the applicant's current city. This needs to connect with parameters "village" and "province" |
| province             | string    | optional  | Equivalent to the applicant's current state. This needs to connect with parameters "village" and "district" |
| isd_code             | int       | optional  | isd_code of mobile/telephone number         |
| telephone            | string    | optional  | local number. Do not include isd_code (country code) as this is already another parameter |
| mail                 | string    | optional  | customer's email address                    |
| occupation           | string    | optional  | applicant's work occupation                 |
| passportnumber       | string    | optional  | Applicant's passport number consisting of alphanumerical characters which is normally found at the top right. This can vary depending on issuing country's passport format |
| passport_issue_date  | string    | optional  | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
| passport_expiry_date | string    | optional  | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
