# Update information of a Park by ID

## `PATCH` /parks/{id}

```
{server_url}/parks/{id}
```

Update an attribute of a park.

### Headers

None

### Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | Integer | Required | A unique identification number for the park instance (positive only) |

### Query Parameters

None

### Request Body

All attributes are individually optional, but the request requires at least one.

| Name | Data Type | Required/Optional | Description | Example |
| --- | --- | --- | --- | --- |
| park_name | String | Optional | The name of the park | Yosemite National Park |
| location | String | Optional | The city or region of the park | Sierra Nevada Mountains |
| habitat | String | Optional | A brief description of the environment | mountains |
| fun fact | String | Optional | A brief fact that makes the park unique | Yosemite Falls, the tallest waterfall in North America, is actually composed of three falls: Upper Yosemite Fall, the middle cascades, and Lower Yosemite Fall.  |
| website | String | Optional | The URL of the official park website | https://www.nps.gov/yose/index.htm |
| id | Integer | Optional | A unique identification number for the park instance (positive only) | 9 |

### Response

| Code | Description |
| --- | --- |
| 200 | Returns the parks object with the matching ID. If there are no parks with the same ID, an empty object is returned. |

## Example

### Example Request

```shell
curl -d "fun%20fact=Yosemite Valley Was Formed by Glaciers." -X PATCH http://localhost:3000/parks/9
```

### Example Response

```shell
{
    "park_name": "Yosemite National Park",
    "location": "Sierra Nevada mountains",
    "habitat": "mountains",
    "fun fact": "Yosemite Valley Was Formed by Glaciers.",
    "website": "https://www.nps.gov/yose/index.htm",
    "id": "9"
}
```
