- Amazon Elastic Load Balancing (**ELB**) is how AWS automagically distributes traffic across all of the configured resources. 
- The ELB is the single point of contact for incoming web traffic and then distributes that traffic to the appropriate resources for handling and processing.  
- This service also works in tandem with Amazon EC2 auto scaling.

## Key Benefits

- Efficient traffic distribution
- Automatic scaling - ELB scales with EC2 when an increase in traffic occurs. 
- Simplified maintenance - Amazon handles maintenance and patching for their ELB systems resolving the need for organizations having to do this with traditional load balancers. 

## Routing Methods

- Round robin
- Least connections - routes traffic to server with fewest active connections. 
- IP Hash - uses IP addresses to consistently route traffic to the same server. 
- Least response time - directs traffic to server with fastest response time (minimizing latency).
## Important to Remember

- ELB works directly with EC2 when traffic scales. It does not add the EC2 instances when traffic goes up. It handles new incoming traffic when the number of servers are increased. 

## Links:

[[Amazon EC2]]

[[Amazon Messaging and Queuing (EventBridge, SQS, SNS)]]

2025111824