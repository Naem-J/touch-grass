# Update Information of a Visitor

## `PATCH` /visitors/{id}

```
{server_url}/visitors/{id}
```

Update individual attributes of a visitor.

### Headers

| Header | Required/Optional | Value |
|--- | --- | --- |
| Content-Type | Optional | application/json |

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | Integer | Required | A unique identification number for the visitor instance (positive only) |

### Query Parameters

None

### Request Body

All attributes are individually optional, but the request requires at least one.

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
curl -d "travel_season=spring" -X PATCH http://localhost:3000/visitors/5
```

### Example Response

```shell
{
  "visitor_id": 5,
  "visitor_type": "Grassland Wanderer",
  "habitat": "chaparrals and grasslands",
  "travel_season": "spring",
  "activities": "hiking, camping, biking",
  "id": 5
}

```
