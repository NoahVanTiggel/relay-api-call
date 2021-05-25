# relay-api-call
This step allows you to easily make api calls to any url. You can specify the http method to use as well as the headers, query parameters and body.
## Parameters
- url: the url to make the call to
- method: the http method to use (get, post, ...)
- headers: the headers to use (as object)
- body: the body to send (as object)
- query: the query parameters to use (as object)
- expects: the http code(s) required for the step to succeed (200 or [ 200, 201 ] ...)
- failon: the http code(s) that will always make the step fail (401 or [ 401, 403 ] ...)
## Usage
To use this step, simply use the image noahvantiggel/relay-api-call in Relay
## Examples
### Headers
```
headers:
  "Content-Type": "application/json"
   Accept: "application/json"
   Authorization: !Secret authkey
```
### Query
```
query:
  x: 1
  y: 2
```
Results in
```
url?x=1&y=2
```
### Body
```
body:
  x: "This is X"
  y: "This is Y"
  z: "This is X"
```
Results in
```
{
  "x": "This is X",
  "y": "This is Y",
  "z": "This is Z"
}
```
