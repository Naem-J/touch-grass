# `/visitors` Resource

The `/visitors` resource stores information about visitor profiles.

### Properties

| Name | Data Type | Required/Optional | Description | Example |
| --- | --- | --- | --- | --- |
| visitor_id | Integer | Required | The visitor type ID number (positive only) | 9 |
| visitor_type | String | Required | A term for the visitor profile type | Redwoods Admirer |
| habitat | String | Required | The preferred habitat for the visitor | forests |
| travel_season | String | Required | The preferred season to travel (`spring`, `summer`, `fall`, `winter`) | spring |
| activites | String | Required | A list of common activities associated with the visitor profile | hiking, biking, horse riding |
| id | Integer | Required | A unique identification number for the visitor instance (positive only) | 9 |

### Endpoints

* [GET visitors](visitors-get-visitors.md)
* [GET visitors by ID](visitors-get-visitors-by-id.md)
* [POST visitors](visitors-post-visitors.md)
* [PUT visitors by ID](visitors-put-visitors-by-id.md)
* [PATCH visitors by ID](visitors-patch-visitors-by-id.md)
* [DELETE visitors by ID](visitors-delete-visitors-by-id.md)

### Other Resources

Also, see [`/parks`](parks.md) resource.
