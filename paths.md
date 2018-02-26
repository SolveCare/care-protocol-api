
<a name="paths"></a>
## Paths

<a name="getbyphonenumberandpasswordusingget"></a>
### Get Account by login
```
GET /accounts
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**password**  <br>*required*|password|string|
|**Query**|**phoneNumber**  <br>*required*|phoneNumber|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[AccountDto](#accountdto)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="confirmphoneusingpost"></a>
### confirmPhone
```
POST /accounts/confirmPhone
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**code**  <br>*required*|code|string|
|**Query**|**phone**  <br>*required*|phone|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[ResponseEntity](#responseentity)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="confirmresettingpasswordcodeusingpost"></a>
### confirmResettingPasswordCode
```
POST /accounts/confirmResettingPasswordCode
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**code**  <br>*required*|code|string|
|**Query**|**phone**  <br>*required*|phone|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[ResponseEntity](#responseentity)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="currentusingget"></a>
### current
```
GET /accounts/current
```


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[AccountDto](#accountdto)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="registerusingpost"></a>
### register
```
POST /accounts/register
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**accountDto**  <br>*required*|accountDto|[AccountDto](#accountdto)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[AccountDto](#accountdto)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="resetpasswordusingpost"></a>
### resetPassword
```
POST /accounts/resetPassword
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**code**  <br>*required*|code|string|
|**Query**|**password**  <br>*required*|password|string|
|**Query**|**phone**  <br>*required*|phone|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[ResponseEntity](#responseentity)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="sendconfirmationcodeusingpost"></a>
### sendConfirmationCode
```
POST /accounts/sendConfirmationCode
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**phone**  <br>*required*|phone|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[SMSAuth](#smsauth)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="getbyidusingget"></a>
### Get Account by id
```
GET /accounts/{id}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|integer (int64)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[AccountDto](#accountdto)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* account-controller


<a name="getbyidusingget_1"></a>
### Get CardScheme by id
```
GET /cardScheme/{id}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|integer (int64)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[CardSchemeDto](#cardschemedto)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* card-scheme-controller


<a name="createusingpost"></a>
### Create Care.Cards
```
POST /cards
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**request**  <br>*required*|request|[CreateCardRequest](#createcardrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[CardDto](#carddto)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* card-controller


<a name="shareusingpost"></a>
### Add Care.Card to account
```
POST /cards/{id}/addToAccount/{accId}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**accId**  <br>*required*|Account id|integer (int64)|
|**Path**|**id**  <br>*required*|Card id|integer (int64)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[CardDto](#carddto)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* card-controller


<a name="getbyowneridusingget"></a>
### Get available decks
```
GET /decks
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**ownerId**  <br>*required*|ownerId|integer (int64)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [DeckDto](#deckdto) > array|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* deck-controller


<a name="getbyidusingget_2"></a>
### Get Deck by id
```
GET /decks/{id}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|integer (int64)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DeckDto](#deckdto)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* deck-controller


<a name="getcardsindeckusingget"></a>
### Get Cards in deck
```
GET /decks/{id}/cards
```


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Path**|**id**  <br>*required*|Deck id|integer (int64)||
|**Query**|**side**  <br>*optional*|Card side|enum (FRONT, BACK)|`"FRONT"`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [CardDto](#carddto) > array|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `*/*`


#### Tags

* deck-controller


<a name="changesettingsusingpost"></a>
### Change deck settings
```
POST /decks/{id}/settings
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|integer (int64)|
|**Body**|**newSettings**  <br>*required*|newSettings|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DeckDto](#deckdto)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* deck-controller


<a name="bookslotusingpost"></a>
### Book schedule slot
```
POST /schedules/book
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**bookSlotRequest**  <br>*required*|bookSlotRequest|[BookSlotRequest](#bookslotrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[ScheduleSlotDto](#scheduleslotdto)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json`


#### Produces

* `*/*`


#### Tags

* schedule-controller


<a name="uploadusingpost"></a>
### upload
```
POST /score/upload
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**FormData**|**file**  <br>*required*|file|file|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[ResponseEntity](#responseentity)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `multipart/form-data`


#### Produces

* `*/*`


#### Tags

* provider-score-controller



