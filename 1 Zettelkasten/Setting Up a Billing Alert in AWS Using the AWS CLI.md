This will assume you already have AWS CLI installed and configured with the appropriate user IDs. 

The following script sets up a warning to fire when the charges exceed $20:

```bash
# Create SNS topic for alerts
aws sns create-topic --name billing-alarm

# Subscribe your email
aws sns subscribe --topic-arn arn:aws:sns:us-east-1:YOUR-ACCOUNT-ID:billing-alarm --protocol email --notification-endpoint your-email@example.com

# Create the alarm (run this in us-east-1 region)
aws cloudwatch put-metric-alarm --alarm-name "Billing-20-Dollar-Limit" \
  --alarm-description "Alert when charges exceed $20" \
  --metric-name EstimatedCharges \
  --namespace AWS/Billing \
  --statistic Maximum \
  --period 21600 \
  --evaluation-periods 1 \
  --threshold 20 \
  --comparison-operator GreaterThanThreshold
```
## Links:

[[Creating an Amazon VPC Mini-Network for Testing]]

2025111128