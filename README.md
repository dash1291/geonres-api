# About the API
You can use this API to consume data containing over 52K artists and the countries they come from. This data was extracted for my own personal project, but anyone can now use it for fun easily through this API.

# Requests

Base URL for all the requests: `http://104.131.173.63`

## GET /countries

This will give you list of countries in the dataset.

## GET /artists/<country>

This will give you list of artists from the specified country.

Sample request:
GET /artists/Austria

Response:

```json
[
  {
    listeners: 1561,
    name: "Markus Schulz & Jochen Miller"
  },
  {
    listeners: 2071,
    name: "Tritonal feat. Meredith Call"
  },
  {
    listeners: 118,
    name: "Blind Of 69"
  },
  {
    listeners: 4271,
    name: "Jonas Goldbaum"
  }
  ...
  ...
]
```

### Additional parameters
These are additional GET query params you can use in your query.

* limit: Limit number of artists per query. Default value for this is 10.
* page: Specify the offset in the list of artists.
* sort: Sort the artists based on number of listeners. Accepted values: "asc"/"desc" for ascending and descending order respectively.

A sample request using these params would be:
`/artists/Austria?limit=5&page=3&sort=desc`

# Get the data

This API was created so that the data can be consumed quickly and easily. Incase the API does not suit your purpose, or you simply want to create your own API, you can write to me that you want the dataset and I will send it you.
