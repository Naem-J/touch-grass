# Update all information in a Parks Object by ID

## `PUT` /parks/{id}

```
{server_url}/parks/{id}
```

Replace all information in the parks object with the matching ID.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | Integer | Required | A unique identification number for the park instance (positive only) |

### Query Parameters

None

### Request Body

| Name | Data Type | Required/Optional | Description | Example |
| --- | --- | --- | --- | --- |
| park_name | String | Required | The name of the park | Yosemite National Park |
| location | String | Required | The city or region of the park | Sierra Nevada Mountains |
| habitat | String | Required | A brief description of the environment | mountains |
| fun fact | String | Required | A brief fact that makes the park unique | Yosemite Falls, the tallest waterfall in North America, is actually composed of three falls: Upper Yosemite Fall, the middle cascades, and Lower Yosemite Fall.  |
| website | String | Required | The URL of the official park website | https://www.nps.gov/yose/index.htm |
| id | Integer | Required | A unique identification number for the park instance (positive only) | 9 |

### Response

| Code | Description |
| --- | --- |
| 200 | Returns the parks object with the information entered as the request body. |

## Example

### Example Request

```shell
curl -d "park_name=Huntington State Beach&location=Huntington Beach, California&habitat=beach and coastline&fun%20fact=The beach also provides a nesting sanctuary for California least terns, an endangered subspecies, and snowy plovers, a threatened species on the West Coast.&website=https://www.parks.ca.gov/?page_id=643&id=9" -X PUT 'http://localhost:3000/parks/9'
```

### Example Response

```shell
{
    "park_name": "Huntington State Beach",
    "location": "Huntington Beach, California",
    "habitat": "beach and coastline",
    "fun fact": "The beach also provides a nesting sanctuary for California least terns, an endangered subspecies, and snowy plovers, a threatened species on the West Coast.",
    "website": "https://www.parks.ca.gov/?page_id=643",
    "id": "9"
}
```
