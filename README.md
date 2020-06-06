# stunning-disco

If the data within the API is publicly accessible then, technically, it is not possible to completely prevent data scraping. However, there is an effective solution that will deter most people/bots: rate limiting (also known as throttling).

Throttling will prevent a certain device from making a defined number of requests within a defined time. Upon exceeding the defined number of requests, a 429 Too Many Attempts HTTP error should be thrown.

Note: It is important to track the device with more than just an IP address as this is not unique to the device and can result in an entire network losing access to an API.

Other less-than-ideal answers include:

Blocking requests based on the user agent string (easy to circumvent)
Generating temporary “session” access tokens for visitors at the front end. This isn’t secure: Storing a secret on the front end can be reverse-engineered, thus allowing anyone to generate access tokens.
