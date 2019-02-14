# IAM secured API Gateway
CloudFormation templates that contain resources for policies and roles that can be used for cross-account 
access to IAM secured API Gateway API.

## Stack commands for client AWS Account:
   
   ```
   aws cloudformation create-stack \
   --stack-name iam-crossaccount-assumerole \
   --template-body file://./api-gateway-client-assumerole-cf.yml \
   --capabilities CAPABILITY_NAMED_IAM
   ```
   
   ```
   aws cloudformation update-stack \
      --stack-name iam-crossaccount-assumerole \
      --template-body file://./api-gateway-client-assumerole-cf.yml \
      --capabilities CAPABILITY_NAMED_IAM
   ```
   
   ```
   aws cloudformation delete-stack \
   --stack-name iam-crossaccount-assumerole
   ```
   
## Stack commands for server AWS Account:

   ```
   aws cloudformation create-stack \
   --stack-name iam-crossaccount-assumerole \
   --template-body file://./api-gateway-service-assumerole-cf.yml \
   --capabilities CAPABILITY_NAMED_IAM
   ```
   
   ```
   aws cloudformation update-stack \
      --stack-name iam-crossaccount-assumerole \
      --template-body file://./api-gateway-service-assumerole-cf.yml \
      --capabilities CAPABILITY_NAMED_IAM
   ```
   
   ```
   aws cloudformation delete-stack \
   --stack-name iam-crossaccount-assumerole
   ```

