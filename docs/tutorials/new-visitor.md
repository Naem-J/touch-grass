# Tutorial: How to Add a New Visitor Profile

The Touch Grass service includes several profiles for common features certain types of visitors are typically interested in. This tutorial adds a new profile to the existing list.

### Get Started

The Touch Grass service contains information about state and national parks in California. In order to access the information, see [Get Started](../overview/quickstart.md).

### Step 1: Run the JSON server

The service currently requires a local JSON server to make API calls. The server runs in a Git Bash instance, but API calls must be performed in a separate window or program.

1. Open Git Bash.

1. Navigate to the cloned folder.

1. Navigate to the `/api` folder.

1. Enter `json-server -w touch-grass-db-source.json`.

### Step 2: Add the New Visitor Type

1. Open Postman.

1. Set the method to **POST**.

1. In the URL field, enter the local domain and resource. For example:
```
http://localhost:3000/visitors
```
NOTE: The default domain is `localhost:3000`, but it can be changed. To verify the domain, check the JSON server introductory text when it was started.

1. In the request body, enter values for each visitors resource property. For example:
```shell
  {
    "visitor_id": "9",
    "visitor_type": "Whale Watcher",
    "habitat": "coastal and marine",
    "travel_season": "summer",
    "activities": "whale watching"
  }
```

1. Select **Send**. The system responds with the same information with an automatically generated ID number.
