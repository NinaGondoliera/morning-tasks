# Load Balancing
​
Can you decide what type of load balancing from the notes might work best for the following situations;
​
- A chat service where users maintain active connections for a while 
* LRT for reasons of fast response during the chat (involves video chat possibly, latency is important)
* RR just to make sure the servers are evenly loaded
​
- An AI image generation API with paid tiers
* SRI to direct the user toward the server that will give them the best experience
* LRT to ensure a propmt response
​
- A social media website that has users all over the world
* SRI to make sure the response matches the time zone, language and other user-specific settings 
​
- An authorisation service that takes the same amount of time for each request
* RR, or LC 
​
- A gaming server that requires low latency
* LRT or also LC, that would ensure the server is not overloaded