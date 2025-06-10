# Get a Park by ID

## `GET` /parks/{id}

```
{server_url}/parks/{id}
```

View the information of a park with the matching ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | Integer | Required | A unique identification number for the park instance (positive only) |

### Query Parameters

None

### Request Body

None

### Response

| Code | Description |
| --- | --- |
| 200 | Returns the parks object with the matching ID. If there are no parks with the same ID, an empty object is returned. |

## Example

### Example Request

```shell
curl http://localhost:3000/parks/1
```

### Example Response

```shell
{
    "park_name": "Channel Islands National Park",
    "location": "Ventura, California",
    "habitat": "coastal and marine",
    "fun fact": "The Channel Islands are home to the island fox, which is an endemic species found nowhere else on Earth.",
    "website": "https://www.nps.gov/chis/index.htm",
    "id": 1
}
```
