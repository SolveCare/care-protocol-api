
<a name="definitions"></a>
## Definitions

<a name="accountdto"></a>
### AccountDto

|Name|Schema|
|---|---|
|**avatarUrl**  <br>*optional*|string|
|**id**  <br>*optional*|integer (int64)|
|**login**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**role**  <br>*optional*|string|


<a name="bookslotrequest"></a>
### BookSlotRequest

|Name|Schema|
|---|---|
|**attendeeId**  <br>*optional*|integer (int64)|
|**scheduleOwnerId**  <br>*optional*|integer (int64)|
|**slotId**  <br>*optional*|integer (int64)|
|**symptoms**  <br>*optional*|string|
|**visitType**  <br>*optional*|enum (NEW_VISIT, FOLLOW_UP_VISIT, REFERRAL_VISIT)|


<a name="cardblockdto"></a>
### CardBlockDto
Provide data for block of requested card


|Name|Description|Schema|
|---|---|---|
|**data**  <br>*optional*|Data structure depends on CardBlock.Type|string|
|**type**  <br>*optional*|Card block type, tells how to process CardBlock.data field|enum (DOCTOR_GENERAL_INFO, DOCTOR_ADDRESS, DOCTOR_RELATIONS_HISTORY, DOCTOR_SHARED_CARDS, SCHEDULE_CALENDAR, SCHEDULE_DETAILS)|


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
|**type**  <br>*optional*|Type of card|enum (DOCTOR_SCORE, DOCTOR_SCHEDULE, DOCTOR_INFO, CLINICAL_RECORDS, LABORATORY_RESULTS)|
|**updatedAt**  <br>*optional*|Timestamp in millis|integer (int64)|


<a name="cardschemedto"></a>
### CardSchemeDto
Represent card structure for Care.Wallet


|Name|Description|Schema|
|---|---|---|
|**createdBy**  <br>*optional*|Account that issued this scheme|integer (int64)|
|**iconUrl**  <br>*optional*|Icon for this type of cards|string|
|**id**  <br>*optional*||integer (int64)|
|**jsonPrivateSideStructure**  <br>*optional*|Private side structure in json|string|
|**jsonPublicSideStructure**  <br>*optional*|Public side structure in json|string|
|**type**  <br>*optional*|Card side type|enum (DOCTOR_SCORE, DOCTOR_SCHEDULE, DOCTOR_INFO, CLINICAL_RECORDS, LABORATORY_RESULTS)|


<a name="cardsidedto"></a>
### CardSideDto
Represent card side structure


|Name|Description|Schema|
|---|---|---|
|**blocks**  <br>*optional*|Blocks that represent the requested card|< [CardBlockDto](#cardblockdto) > array|
|**cardSideType**  <br>*optional*|Card side type|enum (PUBLIC, PRIVATE)|
|**subtitle**  <br>*optional*|Card subtitle|string|
|**title**  <br>*optional*|Card title|string|


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
|**id**  <br>*optional*|integer (int64)|
|**settings**  <br>*optional*|object|
|**type**  <br>*optional*|enum (DOCTOR_SCORE, DOCTOR_SCHEDULE, DOCTOR_INFO, CLINICAL_RECORDS, LABORATORY_RESULTS)|


<a name="linkedcarddto"></a>
### LinkedCardDto

|Name|Schema|
|---|---|
|**iconUrl**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**type**  <br>*optional*|enum (DOCTOR_SCORE, DOCTOR_SCHEDULE, DOCTOR_INFO, CLINICAL_RECORDS, LABORATORY_RESULTS)|
|**url**  <br>*optional*|string|


<a name="scheduleslotdto"></a>
### ScheduleSlotDto

|Name|Schema|
|---|---|
|**finishDate**  <br>*optional*|integer (int64)|
|**finishTime**  <br>*optional*|integer (int64)|
|**id**  <br>*optional*|integer (int64)|
|**startDate**  <br>*optional*|integer (int64)|
|**startTime**  <br>*optional*|integer (int64)|
|**status**  <br>*optional*|enum (FREE, BOOKED, DISABLED)|
|**visitDetails**  <br>*optional*|[VisitDetailsDto](#visitdetailsdto)|


<a name="visitdetailsdto"></a>
### VisitDetailsDto

|Name|Schema|
|---|---|
|**attendeeId**  <br>*optional*|integer (int64)|
|**id**  <br>*optional*|integer (int64)|
|**symptoms**  <br>*optional*|string|
|**visitType**  <br>*optional*|enum (NEW_VISIT, FOLLOW_UP_VISIT, REFERRAL_VISIT)|



