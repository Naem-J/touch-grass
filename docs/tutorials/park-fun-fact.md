# Tutorial: How to Change a Park Fun Fact

Each state and national park has many fun and interesting facts about it. The Touch Grass API only includes one fun fact about each park, but this tutorial describes how to change a fact for a park.

### Get Started

The Touch Grass service contains information about state and national parks in California. In order to access the information, see [Get Started](../overview/quickstart.md).

### Step 1: Run the JSON server

The service currently requires a local JSON server to make API calls. The server runs in a Git Bash instance, but API calls must be performed in a separate window or program.

1. Open Git Bash.

1. Navigate to the cloned folder.

1. Navigate to the `/api` folder.

1. Enter `json-server -w touch-grass-db-source.json`.

### Step 2: Replace the Fun Fact for Joshua Tree National Park

These instructions updates the fun fact associated with Joshua Tree National Park to the following text:
```
The night sky in Joshua Tree National Park is one of the darkest in Southern California, offering unforgettable opportunities to view the Milky Way.
```

1. Open Postman.

1. Set the method to **PATCH**.

1. In the URL, enter the following:
```
http://localhost:3000/parks/3
```
NOTE: The default domain is `localhost:3000`, but it can be changed. To verify the domain, check the JSON server introductory text when it was started.

1. In the Request Body, enter the following:
```shell
  {
    "fun fact" = "The night sky in Joshua Tree National Park is one of the darkest in Southern California, offering unforgettable opportunities to view the Milky Way."
  }
```

1. Select **Send**. A successful response for this request returns all details of the park instance with the new fun fact.
