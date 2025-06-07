# How to Locate a Park

California is the third largest state in the United States and its state and national parks are spread throughout its entire area. Sometimes, geographic and transportation limitations affect where to you may want to go.

### Get Started

The Touch Grass service contains information about state and national parks in California. In order to access the information, follow the [GitHub instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#cloning-a-repository) to clone the [GitHub repository](https://github.com/Naem-J/touch-grass).

### Step 1: Run the JSON server

The service currently requires a local JSON server to make API calls. The server runs in a Git Bash instance, but API calls must be performed in a separate window or program.

1. Open Git Bash.

1. Navigate to the cloned folder.

1. Navigate to the `/api` folder.

1. Enter `json-server -w touch-grass-db-source.json`.

### Look Up a Park by Name

1. Open Postman.

1. Set the method to GET.

1. Enter the following URL and select **Send**. The park location is identified by the `location` attribute.

```
{base URL}/parks?park_name={name of the desired park}
```

For example, to look up the location of Joshua Tree National Park, enter the following:

```
http://localhost:3000/parks?park_name=Joshua%20Tree%20National%20Park
```

This produces the following response:

```
[
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

The location of Joshua Tree National Park is Twentynine Palms, California.

NOTE: The default domain is `localhost:3000`, but it can be changed. To verify the domain, check the JSON server introductory text when it was started.
