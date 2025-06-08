# Get a List of all Visitors

## `GET` /visitors

```
{server_url}/visitors
```

View information from all visitor types.

### Headers

None

### Path Parameters

None

### Query Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| visitor_id | Integer | Required | The visitor type ID number (positive only) |
| visitor_type | String | Required | A term for the visitor profile type |
| habitat | String | Required | The preferred habitat |
| travel_season | String | Required | The preferred season to travel (`spring`, `summer`, `fall`, `winter`) |
| activites | String | Required | A list of common activities associated with the visitor profile |
| id | Integer | Required | A unique identification number for the visitor instance (positive only) |

### Request Body

None

### Response

| Code | Description |
| --- | --- |
| 200 | Returns a collection of parks objects. If there are no visitors on the file, an empty collection is returned. |

## Example

### Example Request

```shell
curl http://localhost:3000/visitors
```

### Example Response

```shell
[
  {
    "visitor_id": 1,
    "visitor_type": "Island Hopper",
    "habitat": "coastal and marine",
    "travel_season": "summer",
    "activities": "kayaking, snorkeling, wildlife watching",
    "id": 1
  },
  {
    "visitor_id": 2,
    "visitor_type": "Forest Trailblazer",
    "habitat": "forests",
    "travel_season": "summer",
    "activities": "hiking, bird watching, camping",
    "id": 2
  },
  {
    "visitor_id": 3,
    "visitor_type": "Dark Sky Discoverer",
    "habitat": "deserts",
    "travel_season": "spring",
    "activities": "stargazing, rock climbing, learning at the visitor center",
    "id": 3
  }
]
```
