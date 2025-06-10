# Delete a Visitor by ID

`DELETE` /visitors/{id}

```
{server_url}/visitors/{id}
```
Delete an visitor object with the matching ID.

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
| 200 | Returns an empty object is returned. |


## Example

### Example Request

```shell
curl -X DELETE http://localhost:3000/visitors/9
```

### Example Response

```shell
{}
```
