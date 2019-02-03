## PayDRC Direct API

This document is intended to provide a guide for third parties who want to use the FreshPay's Direct API (PayDRC) platform for B2C & C2B transactional services.



## Overview

The PayDrc API is organized around REST. The API has predictable resource-oriented URLs, which accepts JSON-encoded request bodies, returns JSON-encoded responses, and uses standard HTTP response codes and verbs.

The API requires you to pass a merchant key and a merchant secrete for every request. 

You can get these keys once you have registered as merchant, on their merchant portal. 


* [Merchant Portal](https://merchant.gofreshbakery.space) : `https://merchant.gofreshbakery.space`

## Base URL


* `https://pay-drc.gofreshbakery.space/`


## Request Headers

* Content-Type: `application/json`


## Endpoints 

All requests should be direct to the `/v3` endpoint.

Request header must be provided with the request.

### Request Actions 

Endpoints for viewing and manipulating the Accounts that the Authenticated User
has permissions to access.

* [B2C-Credit](examples/credit.md) : `POST /v3/`
* [C2B-Debit](examples/debit.md) : `POST /v3/`
* [Verify](exampls/verify.md) : `POST /v3/` 