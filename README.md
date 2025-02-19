# Fakedaq
Fictional stock ticker API written in Go.

# Installation
- Build the app by running `go build`
- Set the rate-limiting environment variable `MAX_LIMIT` to the desired number
- Start the server by running the executable `./fakedaq`

# Routes

 #### Get price quote for a specific stock
`GET /stock/:symbol`

Request 
`curl --header "api-key: test-key" http://localhost:8080/stock/AAPL`

Response
`{"name":"Apple","symbol":"AAPL","price":176.48}`

#### Reset the rate-limit for an API key

Request
`curl --header "api-key: test-key" http://localhost:8080/reset`

Response 
`{"message":"Rate limit has been reset"}`

# Valid symbols
- Livedocs `LDOCS`
- Apple `AAPL`
- Alphabet `GOOGL`
- Microsoft `MSFT`
- Tesla `TSLA`
- Amazon `AMZN`