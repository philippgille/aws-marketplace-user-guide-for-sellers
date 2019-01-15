# Container\-Based Products<a name="container-based-products"></a>

 [AWS Marketplace](https://aws.amazon.com/marketplace/) supports software products that use Docker containers\. Docker containers are an open\-source software technology that provides an additional layer of abstraction and automation over virtualized operating systems such as Linux and Windows Server\. Just as virtual machines are instances of server images, containers are instances of Docker container images\. They wrap server application software in a file system that contains everything it needs to run: code, runtime, system tools, system libraries, and so on\. This guarantees that the software always runs the same, regardless of its environment\. Analogous to Java virtual machines, containers require an underlying platform to provide a translation and orchestration layer while being isolated from the operating system and each other\. 

 AWS Marketplace supports container products that run on any Docker\-compatible runtime, including [Amazon Elastic Container Service](http://aws.amazon.com/ecs/) \(Amazon ECS\) and [Amazon Elastic Container Service for Kubernetes](https://aws.amazon.com/eks/) \(Amazon EKS\)\. These orchestration services enable you to manage and scale container applications on AWS\. Amazon ECS can operate in two modes: [AWS Fargate](https://aws.amazon.com/fargate/) launch type and [Amazon Elastic Compute Cloud](https://aws.amazon.com/ec2/) \(Amazon EC2\) launch type\. Customers can discover your container products through AWS Marketplace or through the Amazon ECS console, and your container images are available in [Amazon Elastic Container Registry](http://aws.amazon.com/ecr/) \(Amazon ECR\)\. 

 You use the **Containers** page on the [AWS Marketplace Management Portal](https://aws.amazon.com/marketplace/management/containers) \(AMMP\) to define container products and create container groups, which represent different fulfillment options for your products\. For each container group, you provide a list of URLs pointing to your container images, which are ingested and scanned\. You then prepare and submit product information by using a product load form \(PLF\)\. You can list free products, bring\-your\-own\-license \(BYOL\) products, and paid products for Amazon ECS\. Only free and BYOL products are supported on Amazon EKS\. If you have an existing AMI\-based container product and want to offer it as a native container product that can run on Amazon ECS or Amazon EKS, you must create a new product in AWS Marketplace\. For your SaaS products that work with container applications, you create a listing for your container\-based agent, whether the SaaS product is already listed or is a new product\. 

 Paid products support the following pricing models: 
+  A fixed monthly price that provides users with unlimited product usage during the following month\. 
+  Usage\-based pricing that is set per hour per Amazon ECS task and is billed per second\. 

 Your products can include multiple container images, but you can set only one price per product\. You use the AWS Marketplace Metering Service API to enforce entitlement for your paid products, and metering for paid products occurs automatically based on usage\. 

 Free and BYOL products don't need to use the [AWS Marketplace Metering Service](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/Welcome.html) because you don't need to validate that the user is entitled to use the product\. However, you can use the API to gain more insight into customer usage of your unpaid products\. 