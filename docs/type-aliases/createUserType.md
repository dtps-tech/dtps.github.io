---
layout: page
title: Create User Type
parent: Types
permalink: /types/createUser
---

# Type Alias : Create User

CreateUserInputDTO: object

## Type declaration

| field                | type      | required  | specifications                              |
|:---------------------|:----------|:----------|:--------------------------------------------|
| title                | string    | yes       | maximum 5 characters eg: Mr, Ms, Dr         |
| first_name           | string    | yes       | Only use Latin alphabet. Must be exact name as SHOWN on passport; otherwise the application may be rejected. If the passport name has any special characters, please transliterate to the Latin alphabet |
| last_name            | string    | yes       | Only use Latin alphabet. Must be exact last name as SHOWN on passport; otherwise the application may be rejected. If the passport name has any special characters, please transliterate to the Latin alphabet|
| gender               | string    | yes       | accepted values - Male, Female, Other, None |
| dob                  | string    | yes       | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
| place_of_birth       | string    | yes       | full country name, maximum 50 characters    |
| birth_country        | string    | yes       | 2-digit ISO format eg: Australia = *AU*     |
| village              | string    | yes       | Equivalent to the applicant's current street address. This needs to connect with the other parameters "district" and "province |
| district             | string    | yes       | Equivalent to the applicant's current city. This needs to connect with parameters "village" and "province" |
| province             | string    | yes       | Equivalent to the applicant's current state. This needs to connect with parameters "village" and "district" |
| isd_code             | int       | yes       | isd_code of mobile/telephone number         |
| telephone            | string    | yes       | local number. Do not include isd_code (country code) as this is already another parameter |
| mail                 | string    | yes       | customer's email address                    |
| occupation           | string    | yes       | applicant's work occupation                 |
| passportnumber       | string    | yes       | Applicant's passport number consisting of alphanumerical characters which is normally found at the top right. This can vary depending on issuing country's passport format |
| passport_issue_date  | string    | yes       | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
| passport_expiry_date | string    | yes       | Exact date as shown on passport; although please transpose to the format required by our API which is DD/MM/YYYY |
