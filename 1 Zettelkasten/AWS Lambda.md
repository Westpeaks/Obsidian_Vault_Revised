
- Lambda is a serverless compute service that runs code based on a series of parameters. It handles service requests and scales automatically based on the number of requests. You are only charged for the compute time consumed. Lambda will handle all infrastructure required to execute the code you configure it to execute. 

# How Lambda Works

![[lambda.png]]

## Key Components Involved

- Lambda function
- Triggers
- Runtimes
 
## Real World Examples

- A social media company uses Lambda to process images uploaded by users. When a photo is uploaded, Lambda is triggered to resize the image, apply filters, and save it in an optimized format to storage.
  
- A news aggregator uses Lambda to fetch and process news articles from multiple sources, then it tailors recommendations based on user preferences. When a user opens the application or performs a search, Lambda functions are triggered to retrieve data, run personalization logic, and return relevant content.
  
- A gaming company uses Lambda to handle in-game events like player actions, game state changes, and real-time leader board updates. Each event (like scoring a point or unlocking an achievement) triggers a Lambda function that updates player data and game status.

## Links:

[[AWS Unmanaged vs Managed Services]]

2025111909