# `/parks` Resource

The `/parks` resource stores information about state and national parks in California.

### Properties

| Name | Data Type | Required/Optional | Description | Example |
| --- | --- | --- | --- | --- |
| park_name | String | Optional | The name of the park | Yosemite National Park |
| location | String | Optional | The city or region of the park | Sierra Nevada Mountains |
| habitat | String | Optional | A brief description of the environment | mountains |
| fun fact | String | Optional | A brief fact about what makes the park unique | Yosemite Falls, the tallest waterfall in North America, is actually composed of three falls: Upper Yosemite Fall, the middle cascades, and Lower Yosemite Fall.  |
| website | String | Optional | The URL of the official park website | https://www.nps.gov/yose/index.htm |
| id | Integer | Optional | A unique identification number for the park instance (positive only) | 9 |

### Endpoints

* [GET parks](parks-get-parks.md)
* [GET parks by ID](parks-get-parks-by-id.md)
* [POST parks](parks-post-parks.md)
* [PUT parks by ID](parks-put-parks-by-id.md)
* [PATCH parks by ID](parks-patch-parks-by-id.md)
* [DELETE parks by ID](parks-delete-parks-by-id.md)

### Other Resources

Also, see [`/visitors`](visitors.md) resource.
