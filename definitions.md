
<a name="definitions"></a>
## Definitions

<a name="accountdto"></a>
### AccountDto

|Name|Schema|
|---|---|
|**email**  <br>*optional*|string|
|**id**  <br>*optional*|integer (int64)|
|**name**  <br>*optional*|string|
|**password**  <br>*optional*|string|
|**phoneNumber**  <br>*optional*|string|
|**roles**  <br>*optional*|< string > array|
|**settings**  <br>*optional*|[AccountSettingsDto](#accountsettingsdto)|
|**statuses**  <br>*optional*|< enum (ENABLED, DISABLED, EMAIL_CONFIRMATION_WAITING, PHONE_CONFIRMATION_WAITING) > array|
|**surname**  <br>*optional*|string|


<a name="accountsettingsdto"></a>
### AccountSettingsDto

|Name|Schema|
|---|---|
|**avatarUrl**  <br>*optional*|string|
|**deckIds**  <br>*optional*|< integer (int64) > array|


<a name="bookslotrequest"></a>
### BookSlotRequest

|Name|Schema|
|---|---|
|**attendeeId**  <br>*optional*|integer (int64)|
|**ownerId**  <br>*optional*|integer (int64)|
|**slotId**  <br>*optional*|integer (int64)|
|**symptoms**  <br>*optional*|string|
|**visitType**  <br>*optional*|enum (NEW, FOLLOW_UP, REFERRAL)|


<a name="cardblockdto"></a>
### CardBlockDto
Provide data for block of requested card


|Name|Description|Schema|
|---|---|---|
|**data**  <br>*optional*|Data structure depends on CardBlock.Type|object|
|**isPinned**  <br>*optional*|Ability to pin block to the card header  <br>**Example** : `false`|boolean|
|**type**  <br>*optional*|Card block typeMetadata, tells how to process CardBlock.data field|string|


<a name="cardcornerdto"></a>
### CardCornerDto
Represent card side structure


|Name|Schema|
|---|---|
|**iconUrl**  <br>*optional*|string|
|**isEnabled**  <br>*optional*|boolean|


<a name="carddto"></a>
### CardDto
Represent Care.Card for Care.Wallet


|Name|Description|Schema|
|---|---|---|
|**createdAt**  <br>*optional*|Timestamp in millis|integer (int64)|
|**id**  <br>*optional*||integer (int64)|
|**issuedBy**  <br>*optional*|Account that issued this card|integer (int64)|
|**links**  <br>*optional*|Links to another cards|< [LinkedCardDto](#linkedcarddto) > array|
|**ownedBy**  <br>*optional*|Account that owned this card|integer (int64)|
|**side**  <br>*optional*|Card side|[CardSideDto](#cardsidedto)|
|**typeMetadata**  <br>*optional*|Type of card|[CardTypeMetadata](#cardtypemetadata)|
|**updatedAt**  <br>*optional*|Timestamp in millis|integer (int64)|


<a name="cardschemedto"></a>
### CardSchemeDto
Represent card structure for Care.Wallet


|Name|Description|Schema|
|---|---|---|
|**createdBy**  <br>*optional*|Account that issued this scheme|integer (int64)|
|**iconUrl**  <br>*optional*|Icon for this typeMetadata of cards|string|
|**id**  <br>*optional*||integer (int64)|
|**jsonPrivateSideStructure**  <br>*optional*|Private side structure in json|string|
|**jsonPublicSideStructure**  <br>*optional*|Public side structure in json|string|
|**type**  <br>*optional*|Card side typeMetadata|[CardTypeMetadata](#cardtypemetadata)|


<a name="cardsidedto"></a>
### CardSideDto
Represent card side structure


|Name|Description|Schema|
|---|---|---|
|**blocks**  <br>*optional*|Blocks that represent the requested card|< [CardBlockDto](#cardblockdto) > array|
|**cardSideType**  <br>*optional*|Card side typeMetadata|enum (FRONT, BACK)|
|**flipCorner**  <br>*optional*||[CardCornerDto](#cardcornerdto)|
|**infoCorner**  <br>*optional*||[CardCornerDto](#cardcornerdto)|
|**linkCorner**  <br>*optional*||[CardCornerDto](#cardcornerdto)|
|**shareCorner**  <br>*optional*||[CardCornerDto](#cardcornerdto)|
|**subtitle**  <br>*optional*|Card subtitle|string|
|**title**  <br>*optional*|Card title|string|


<a name="cardtypemetadata"></a>
### CardTypeMetadata

|Name|Schema|
|---|---|
|**iconUrl**  <br>*optional*|string|
|**id**  <br>*optional*|integer (int64)|
|**title**  <br>*optional*|string|
|**type**  <br>*optional*|string|


<a name="createcardrequest"></a>
### CreateCardRequest

|Name|Schema|
|---|---|
|**cardSchemeId**  <br>*optional*|integer (int64)|
|**issuedBy**  <br>*optional*|integer (int64)|
|**ownedBy**  <br>*optional*|integer (int64)|


<a name="deckdto"></a>
### DeckDto

|Name|Schema|
|---|---|
|**cardsCount**  <br>*optional*|integer (int32)|
|**faceCard**  <br>*optional*|[CardDto](#carddto)|
|**id**  <br>*optional*|integer (int64)|
|**settings**  <br>*optional*|object|
|**typeMetadata**  <br>*optional*|[CardTypeMetadata](#cardtypemetadata)|


<a name="linkedcarddto"></a>
### LinkedCardDto

|Name|Schema|
|---|---|
|**deckId**  <br>*optional*|integer (int64)|
|**iconUrl**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**ownerId**  <br>*optional*|integer (int64)|
|**type**  <br>*optional*|[CardTypeMetadata](#cardtypemetadata)|


<a name="62325ee98a6882a3a64e3a848f7d61df"></a>
### Page«CardDto»

|Name|Schema|
|---|---|
|**content**  <br>*optional*|< [CardDto](#carddto) > array|
|**first**  <br>*optional*|boolean|
|**last**  <br>*optional*|boolean|
|**number**  <br>*optional*|integer (int32)|
|**numberOfElements**  <br>*optional*|integer (int32)|
|**size**  <br>*optional*|integer (int32)|
|**sort**  <br>*optional*|[Sort](#sort)|
|**totalElements**  <br>*optional*|integer (int64)|
|**totalPages**  <br>*optional*|integer (int32)|


<a name="responseentity"></a>
### ResponseEntity

|Name|Schema|
|---|---|
|**body**  <br>*optional*|object|
|**statusCode**  <br>*optional*|enum (100, 101, 102, 103, 200, 201, 202, 203, 204, 205, 206, 207, 208, 226, 300, 301, 302, 303, 304, 305, 307, 308, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 426, 428, 429, 431, 451, 500, 501, 502, 503, 504, 505, 506, 507, 508, 509, 510, 511)|
|**statusCodeValue**  <br>*optional*|integer (int32)|


<a name="smsauth"></a>
### SMSAuth

|Name|Schema|
|---|---|
|**createdAt**  <br>*optional*|string (date-time)|
|**expiredAt**  <br>*optional*|string (date-time)|
|**id**  <br>*optional*|integer (int64)|
|**phoneNumber**  <br>*optional*|string|
|**status**  <br>*optional*|enum (CODE_SENT, CODE_CONFIRMED)|


<a name="scheduleslotdto"></a>
### ScheduleSlotDto

|Name|Schema|
|---|---|
|**finishTimestamp**  <br>*optional*|integer (int64)|
|**id**  <br>*optional*|integer (int64)|
|**startTimestamp**  <br>*optional*|integer (int64)|
|**status**  <br>*optional*|enum (FREE, BOOKED, DISABLED)|
|**visitDetails**  <br>*optional*|[VisitDetailsDto](#visitdetailsdto)|


<a name="sort"></a>
### Sort
*Type* : object


<a name="visitdetailsdto"></a>
### VisitDetailsDto

|Name|Schema|
|---|---|
|**attendeeId**  <br>*optional*|integer (int64)|
|**id**  <br>*optional*|integer (int64)|
|**symptoms**  <br>*optional*|string|
|**visitType**  <br>*optional*|enum (NEW, FOLLOW_UP, REFERRAL)|



