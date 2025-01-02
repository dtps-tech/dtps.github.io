---
layout: home
title: Home
permalink: /home/
nav_order: 1
---

# Introduction

The DTPS API (v1.0) provides a robust set of RESTful endpoints to support operations related to user account management, card activation, application processing, balance checks, transaction histories, top-up management, and partner float management. It is secured through API key, secret, and signature-based authentication.

This API is tailored for seamless integration with systems requiring dynamic management of user accounts and debit card functionalities, offering streamlined processes for digital card issuance, transactions, and float-based resource management.

# Key Features and Endpoints

## User Management

1. Create User (POST /user/create): Add a new user with detailed personal and contact information. 
2. Update User Details (POST /user/update/{userId}): Modify user details.
3. Upload User Documents (POST /user/document/upload): Upload identity verification documents such as passport and selfies.
4. Get User Details (GET /user/{userId}): Retrieve information about a specific user.
5. List All Users (GET /user/list): Fetch all registered users with pagination options.

## Card Application

1. Get Available Cards (GET /card/list): Retrieve a list of available cards for issuance.
2. Apply for a Card (POST /card/application/apply): Initiate a card application after completing user creation and document upload.
3. Apply Without KYC Approval (POST /card/application/noverify/apply): Submit an application bypassing KYC verification.
4. List All Applications (GET /card/application/list): View all card applications with pagination.
5. Retrieve a Specific Application (GET /card/application/{cardapplicationId}): Fetch details of a specific application.

## Card Operations

1. Activate Card (POST /card/activate): Activate a card using a base64-encoded image of the user holding the card and passport together.
2. Check Card Balance: <br>
    a. By Card ID (GET /card/balance/id/{cardId}) <br>
    b. By Card Number (GET /card/balance/{cardnumber})

3. View Transaction History: <br>
    a. By Card ID (GET /card/txnhistory/id/{cardId}) <br>
    b. By Card Number (GET /card/txnhistory/{cardnumber})

## Top-Ups

1. Apply for Top-Up (POST /card/topup/apply): Submit a top-up request for a specific card.
2. List All Top-Up Applications (GET /card/topup/list): View all top-up applications with pagination.

## Float Management

Partners are required to maintain a float balance to process card applications and top-ups. The float serves as a prepaid account, and the following deductions are made: <br>
**Card Application Costs:** Deducted from the float for every card issued. <br>
**Top-Up Amounts:** Includes loading fees and processing charges. <br>

Float balances can be managed through the partner management module in the API, ensuring uninterrupted service for card operations.

## Authentication and Security

The API enforces security using the following headers: <br>
**X-Api-Key**: API key for authentication. <br>
**X-Api-Signature**: Signature for request validation.

## Response and Schema Highlights

Standardized responses are defined in the responses schema, such as OkResponse.
Objects like CardPurchaseApplication, User, and Transaction provide structured data formats for interaction.
