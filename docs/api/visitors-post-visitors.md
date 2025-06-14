# Add a New Visitor Profile

## `POST` /visitors

```
{server_url}/visitors
```

Create a new visitors object.

### Headers

| Header | Required/Optional | Value |
|--- | --- | --- |
| Content-Type | Optional | application/json |

### Path Parameters

None

### Query Parameters

None

### Request Body

| Name | Data Type | Required/Optional | Description | Example |
| --- | --- | --- | --- | --- |
| visitor_id | Integer | Required | The visitor type ID number (positive only) | 9 |
| visitor_type | String | Required | A term for the visitor profile type | Redwoods Admirer |
| habitat | String | Required | The preferred habitat for the visitor | forests |
| travel_season | String | Required | The preferred season to travel (`spring`, `summer`, `fall`, `winter`) | spring |
| activites | String | Required | A list of common activities associated with the visitor profile | hiking, biking, horse riding |
| id | Integer | Required | A unique identification number for the visitor instance (positive only) | 9 |

### Response

| Code | Description |
| --- | --- |
| 200 | Returns the visitors object with the matching ID. If there are no visitors with the same ID, an empty object is returned. |

## Example

### Example Request

```shell
curl -d "visitor_id=9&visitor_type=Whale Watcher&habitat=coastal and marine&travel_season=summer&activities=whale watching&id=9" -X POST http://localhost:3000/visitors
```

### Example Response

```shell
{
  "visitor_id": "9",
  "visitor_type": "Whale Watcher",
  "habitat": "coastal and marine",
  "travel_season": "summer",
  "activities": "whale watching",
  "id": "9"
}

```
