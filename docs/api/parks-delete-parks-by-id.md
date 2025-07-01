---
layout: default
title: Delete a Park by ID
description: Delete a park instance from the parks resource.
---

# `DELETE` /parks/{id}

```
{server_url}/parks/{id}
```

## Headers

None

## Path Parameters

| Name | Data Type | Required/Optional | Description |
| --- | --- | --- | --- |
| id | integer | Required | A unique identification number for the park instance (positive only) |

## Query Parameters

None

## Request Body

None

## Response

| Code | Description |
| --- | --- |
| 200 | Returns an empty object is returned. |

# Example

## Example Request

```shell
curl -X DELETE http://localhost:3000/parks/9
```

## Example Response

```json
{}
```
