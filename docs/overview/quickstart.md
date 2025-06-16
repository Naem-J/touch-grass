# Get Started

Since this is a mock API, set up your own development system on your computer to emulate a host domain.

### Prerequisites

To set up your own development system, ensure you have the following:

* A [GitHub](https://github.com/) account
* [Git](https://git-scm.com/downloads)
* [node.js](https://nodejs.org/en/download)
* [json-server](https://www.npmjs.com/package/json-server)
* [curl](https://curl.se/download.html)
* Text editor (for example, GitHub Desktop)

### Copy the Touch Grass Repository

The Touch Grass API is an open service and available to multiple subscribers. To ensure data is not inadvertently changed between subscribers, create a copy of the repository for your own use.

1. [Fork the Touch Grass repository.](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#forking-a-repository)

1. [Clone the forked repository.](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#cloning-your-forked-repository)

### Test the JSON Server

To ensure the service works on your local computer, perform the following test:

1. Open Git Bash.
1. Navigate to the cloned repository.
1. Navigate to the .json file.
```shell
cd api
```
1. Enter the following:
```shell
json-server -w touch-grass-db-source.json
```
1. Note the "Home" domain in the response. For example:
```
  \{^_^}/ hi!

  Loading touch-grass-db-source.json
  Done

  Resources
  http://localhost:3000/parks
  http://localhost:3000/visitors

  Home
  http://localhost:3000
```
1. Without closing the current Git Bash window, open a new Git Bash window.
1. Run a test `GET` request. For example:
```shell
curl http://localhost:3000/parks
```
If you see a response with park information, the test is successful. For example:
```
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
      }
    ]
```
