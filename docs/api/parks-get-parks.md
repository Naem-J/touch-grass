# Get a List of Parks

## `GET` /parks

```
{server_url}/parks
```

View information from all parks.

### Headers

None

### Path Parameters

None

### Query Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| park_name | String | Required | The name of the park |
| location | String | Required | The city or region of the park |
| habitat | String | Required | A brief description of the environment |
| fun fact | String | Required | A brief fact that makes the park unique |
| website | String | Required | The URL of the official park website |
| id | Integer | Required | A unique identification number for the park instance (positive only) |

### Request Body

None

### Response

| Code | Description |
| --- | --- |
| 200 | Returns a collection of parks objects. If there are no parks on the file, an empty collection is returned. |

## Example

### Example Request

```shell
curl http://localhost:3000/parks
```

### Example Response

```shell
[
    {
        "park_name": "Channel Islands National Park",
        "location": "Ventura, California",
        "habitat": "coastal and marine",
        "fun fact": "The Channel Islands are home to the island fox, which is an endemic species found nowhere else on Earth.",
        "website": "https://www.nps.gov/chis/index.htm",
        "id": 1
    },
    {
        "park_name": "Sequoia & Kings Canyon National Parks",
        "location": "Three Rivers, California",
        "habitat": "forests",
        "fun fact": "Sequoia and Kings Canyon are home to nearly 300 native animal species, including the alpine chipmunk.",
        "website": "https://www.nps.gov/seki/index.htm",
        "id": 2
    },
    {
        "park_name": "Joshua Tree National Park",
        "location": "Twentynine Palms, California",
        "habitat": "deserts",
        "fun fact": "Two distinct desert ecosystems, the Mojave and the Colorado, come together in Joshua Tree National Park.",
        "website": "https://www.nps.gov/jotr/index.htm",
        "id": 3
    }
]
```
