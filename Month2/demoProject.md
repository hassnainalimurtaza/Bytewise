# Project: Bike Sikhoo
---

## Abstact : 
Now a days fuel prices and public transport is not feasible to the women to use to daily comute , its easier to already available connivance at home to travel, so build an web app which will register applicants and provide them physical trainings.
### Web stack:
* Html ,css, js 
* java,springboot for backend apis
* Amazon rds 

# Amazon Web Services:
General Purpose, Spot Instances for web applications as spot saves us the cost because we do not require daily access to the app only required twice a year during the training period for women's bike riding, also the processing of records is required and can be achieved under general purpose(t4g.2xlarge) Amazon Simple Queue Service (Amazon SQS) will be used inter communication of components.

# Global Infrastructure and Reliability:
Region “Bahrain”(me-south-1) closest to pakistan will be supported and lowest latency(52 ms) as compared to mumbai(114 ms)  , Network ACLs will be used to allow admins to access few functionalities related to addition and deletion of services of the training program.AWS CloudFormation will be used to automatically configure our instances in case of increase of traffic,alongwith elasticbeanstalk for easy management of aws infra.

# Storage:
Amazon RDS will be used as its a relational database and our schema will only be storing people information registered for the training programs,alongwith Amazon Elastic Block Store (EBS) in case of new instance creations by autoscallings

# Security:
As shared responsibility model is being used in aws cloud infra,will use IAM permissions to access the sensitive data of the consumers , furthermore aws organizations can be set for account related tasks

# Monitoring and Analytics:
For monitoring cloudwatch will be used to study the web application’s working under load , also cloud trail can be used for backend api responses under high traffic situations.For improvement of the app trusted advisor can be utilized to save budget/costs of operations,which can be compared with the consolidated billing service/billing dashboard
