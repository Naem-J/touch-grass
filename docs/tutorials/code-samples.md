# Code Samples

### Find a Park Location
The following code can be integrated into an HTML file to retrieve the location of a requested park. The HTML file will require a button to trigger the request.

```html
<!--Finds the location property of the park resource instance named Joshua Tree National Park upon the press of a button with the id of "getLocationBtn" -->
<script>
    document.getElementById("getLocationBtn").addEventListener("click", function () {
      fetch("http://localhost:3000/parks?park_name=Joshua%20Tree%20National%20Park")
        .then(response => {
          if (!response.ok) {
            throw new Error("Network response was not ok");
          }
          return response.json();
        })
        .then(data => {
          document.getElementById("output").textContent = "Location: " + data.location;
        })
        .catch(error => {
          document.getElementById("output").textContent = "Error: " + error.message;
        });
    });
  </script>
```
