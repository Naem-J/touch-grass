# GET Visitors by ID

## `GET` /visitors/{id}

```
{server_url}/visitors/{id}
```

View the information of a visitor type with the matching ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | Integer | Required | A unique identification number for the visitor instance (positive only) |

### Query Parameters

None

### Request Body

None

### Response

| Code | Description |
| --- | --- |
| 200 | Returns the parks object with the matching ID. If there are no visitors with the same ID, an empty object is returned. |

## Example

### Example Request

```shell
curl http://localhost:3000/visitors/1
```

### Example Response

```shell
{
  "visitor_id": 1,
  "visitor_type": "Island Hopper",
  "habitat": "coastal and marine",
  "travel_season": "summer",
  "activities": "kayaking, snorkeling, wildlife watching",
  "id": 1
}

```
