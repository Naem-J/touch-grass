# Add a New Park

## `POST` /parks

```
{server_url}/parks
```

Create a new park object.

### Headers

None

### Path Parameters

None

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
curl -d "park_name=Yosemite National Park&location=Sierra Nevada mountains&habitat=mountains&fun%20fact=Yosemite Falls, the tallest waterfall in North America, is actually composed of three falls: Upper Yosemite Fall, the middle cascades, and Lower Yosemite Fall.&website=https://www.nps.gov/yose/index.htm&id=10" -X POST http://localhost:3000/parks
```

### Example Response

```shell
{
    "park_name": "Yosemite National Park",
    "location": "Sierra Nevada mountains",
    "habitat": "mountains",
    "fun fact": "Yosemite Falls, the tallest waterfall in North America, is actually composed of three falls: Upper Yosemite Fall, the middle cascades, and Lower Yosemite Fall.",
    "website": "https://www.nps.gov/yose/index.htm",
    "id": "9"
}
```
