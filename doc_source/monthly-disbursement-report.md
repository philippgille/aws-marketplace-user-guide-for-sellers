# Monthly Disbursement Report<a name="monthly-disbursement-report"></a>

 The monthly disbursement report provides information about funds that we collected and disbursed to your bank accounts since the previous disbursement\. Disbursements can include customer payments or refunds for a subscription to your product, and some taxes collected or refunded to the customer\. You don't receive disbursement of funds until the funds are collected from the customer\. Different customers have different payment terms with AWS, so some of the funds in each of the uncollected age categories might not be due from the customer\. 

 Refunds appear as negative amounts because the money is returned to your customer after you authorize a refund\. 

 This report is available on the AWS Marketplace Management Portal under the **Reports** tab\. If you're enrolled in the AWS Marketplace commerce analytics service, you can use API calls to pull down sections of this report\. For more information, see [AWS Marketplace Commerce Analytics Service](commerce-analytics-service.md)\. 

## Publication Schedule<a name="publication-schedule-3"></a>

 This report is published monthly at 00:00 UTC 3 days after a successful disbursement to your bank account\. We consider the disbursement successful after the disbursement settlement is recorded with your bank\. 

**Topics**
+ [Publication Schedule](#publication-schedule-3)
+ [Section 1: Disbursed Amount by Product](#section-1-disbursed-amount-by-product)
+ [Section 2: Disbursed Amount by Customer Geography](#section-2-disbursed-amount-by-customer-geography)
+ [Section 3: Disbursed Amount by Instance Hours](#section-3-disbursed-amount-by-instance-hours)
+ [Section 4: Age of Uncollected Funds](#section-4-age-of-uncollected-funds)
+ [Section 5: Age of Past Due Funds](#age-of-past-due-funds)
+ [Section 6: Age of Disbursed Funds](#section-5-age-of-disbursed-funds)

## Section 1: Disbursed Amount by Product<a name="section-1-disbursed-amount-by-product"></a>

 This section lists data for disbursements by product\. For each row, the Net Amount column is equal to the SellerRev column minus the AWSRefFee column\. When a refund is given to a customer, the Net Amount column is a negative number that is equal to the SellerRevRefund column minus the AWSRefFeeRefund column\. US sales and use tax that is collected or refunded is in the SellerUSSalesTax or SellerUSSalesTaxRefund column and isn't included in the calculation of the Net Amount column\. 


|  Column Name  |  Available for All Sellers  |  Available for Sellers in the Enhanced Data Sharing Program  |  Description  | 
| --- | --- | --- | --- | 
|  Product  |  ✔  |  ✔  |  The title of the product\.  | 
|  Product Code  |  ✔  |  ✔  |  The unique identifier for the software product\. | 
|  SellerRev  |  ✔  |  ✔  |  The amount that is billed to the customer for the usage or monthly fees of the product\.  | 
|  AWSRefFee  |  ✔  |  ✔  |  The amount of the AWS Marketplace fee\.  | 
|  SellerRevRefund  |  ✔  |  ✔  |  The amount of the software subscription cost that is refunded to customers if any refunds were processed during the data coverage period\.  | 
|  AWSRefFeeRefund  |  ✔  |  ✔  |  The amount of the AWS Marketplace fee that is refunded if any refunds were processed during the data coverage period\. | 
|  SellerRevCredit  |  ✔  |  ✔  | The AWS credits that AWS Marketplace placed on the customer's account\.  | 
|  AWSRefFeeCredit  |  ✔  |  ✔  |  The AWS credits that AWS Marketplace placed on your account\.  | 
|  Net Amount  |  ✔  |  ✔  |  The total funds that we disbursed to you\. This column is equal to the SellerRev column minus the AWSRefFee column\. When a refund is given to a customer, this column is a negative number equal to the SellerRevRefund column minus the AWSRefFeeRefund column\.  | 
|  Transaction Reference ID  |  ✔  |  ✔  |  A unique identifier for the transaction that helps you correlate transactions across AWS Marketplace reports\.  | 
|  SellerUSSalesTax  |  ✔  |  ✔  |  The total amount of US sales and use tax that is billed for this transaction\.  | 
|  SellerUSSalesTaxRefund  |  ✔  |  ✔  |  The total amount of US sales and use tax that is refunded for this transaction if a refund was processed\.  | 
|  Customer AWS Account Number  |   |  ✔  | The ID of the account that the software charges are billed to\.  | 
|  Customer Country  |   |  ✔  | The two\-character country code that is associated with the account that the software charges are billed to\. This report uses ISO 3166\-1 alpha\-2 standard\.  | 
|  Customer State  |   |  ✔  | The billing address state that is associated with the account that the software charges are billed to\. | 
|  Customer City  |   |  ✔  | The billing address city that is associated with the account that software charges are billed to\. | 
|  Customer Zip Code  |   |  ✔  | The billing address postal code that is associated with the account that the software charges are billed to\. | 
|  Customer Email Domain  |   |  ✔  |  The email domain that is associated with the account that the software charges are billed to\. For example, if the email address is liu\-jie@example\.com, the entry is example\.com\. | 
|  Solution Title  |  ✔  |  ✔  |  The name of the solution\.  | 
|  Solution ID  |  ✔  |  ✔  |  The unique identifier for the solution\.  | 
|  Launch Type Description  |  ✔  |  ✔  |  The type of instance that the customer launched\. This is Amazon EC2 or AWS Fargate\.  | 
|  Container Hours  |  ✔  |  ✔  |  The aggregate partial hours per Region by launch type\.  | 
|  Payer Reference ID  |  ✔  |  ✔  |  A unique identifier that isn't the account ID\. It's associated with the account that fees are billed to\. It helps with tracking usage, revenue, and subscriptions by customers across all of the AWS Marketplace financial reports\.  | 
|  Payer Address ID  |   |  ✔  |  A unique identifier that represents the customer's address\. | 

## Section 2: Disbursed Amount by Customer Geography<a name="section-2-disbursed-amount-by-customer-geography"></a>

 This section lists data for disbursements by the customer's geographic location\. The amount in the Disbursed Amount column is equal to the sum of the entries in the Postal Code column\. The sum of the entries in the Net Amount By Tax Location column is equal to the sum of the entries in the Postal Code column minus the sum of the entries in the Seller U\.S\. Sales Tax column and the Seller U\.S\. Sales Tax Refund columns\. 


|  Column Name  |  Available for All Sellers  |  Available for Sellers in the Enhanced Data Sharing Program |  Description  | 
| --- | --- | --- | --- | 
|  Settlement ID  |  ✔  |  ✔  |  The unique identifier of the disbursement\.  | 
|  Settlement Period Start Date  |  ✔  |  ✔  |  The starting date and time of the disbursement period\.  | 
|  Settlement Period End Date  |  ✔  |  ✔  |  The ending date and time of the disbursement period\.  | 
|  Deposit Date  |  ✔  |  ✔  |  The date and time when the disbursement occurred\.  | 
|  Disbursed Amount  |  ✔  |  ✔  |  The total amount of the disbursement, and is equal to the total of the Postal Code column in this section of the report\. | 
|  Country Code  |  ✔  |  ✔  | The two\-character country code that is associated with the account that the software charges are billed to\. This report uses ISO 3166\-1 alpha\-2 standard\.  | 
|  State or Region  |  ✔  |  ✔  | The billing address state that is associated with the account that the software charges are billed to\. | 
|  City  |  ✔  |  ✔  | The billing address city that is associated with the account that software charges are billed to\. | 
|  Postal Code  |  ✔  |  ✔  |  The total funds that are disbursed to the seller, grouped by postal code\. The total of this column is equal to the Disbursed Amount column in this section of the report\.  | 
|  Net Amount by Tax Location  |  ✔  |  ✔  |  The total funds that are disbursed to the seller by tax location, less AWS Marketplace fees, refunds, and US sales and use tax\.  | 
|  Gross Amount by Tax Location  |  ✔  |  ✔  |  The total funds that are disbursed to the seller by tax location\.  | 
|  Seller U\.S\. Sales Tax  |  ✔  |  ✔  |  The total amount of US sales and use tax that is disbursed to the seller for the transaction, grouped by location\.  | 
|  Seller U\.S\. Sales Tax Refund  |  ✔  |  ✔  |  The total amount of US sales and use tax that is refunded to the customer for the transaction, grouped by location\.  | 

## Section 3: Disbursed Amount by Instance Hours<a name="section-3-disbursed-amount-by-instance-hours"></a>

 This section lists data for disbursements by Amazon EC2 instance hours\. 


|  Column Name  |  Available for All Sellers  |  Available for Sellers in the Enhanced Data Sharing Program  |  Description  | 
| --- | --- | --- | --- | 
|  Product  |  ✔  |  ✔  |  The title of the product\. | 
|  Product Code  |  ✔  |  ✔  |  The unique identifier for the software product\.  | 
|  Usage Type Description  |  ✔  |  ✔  |  The description of the usage, including offer type, Region, and instance type\.  | 
|  Rate  |  ✔  |  ✔  |  The software rate per hour for the offer type, Region, and instance type\.  | 
|  User Count  |  ✔  |  ✔  |  The number of unique customers using the offer type, Region, and instance type\.  | 
|  Instance Hours  |  ✔  |  ✔  |  The number of hours that the instance consumed for the offer type, Region, and instance type\.  | 
|  Solution Title  |  ✔  |  ✔  |  The name of the solution\.  | 
|  Solution ID  |  ✔  |  ✔  |  The unique identifier for the solution\.  | 

## Section 4: Age of Uncollected Funds<a name="section-4-age-of-uncollected-funds"></a>

 This section lists data for uncollected funds, organized by the age\. Uncollected funds might include amounts that aren't due yet\. 


|  Column Name  |  Available for All Sellers |  Available for Sellers in the Enhanced Data Sharing Program  |  Description  | 
| --- | --- | --- | --- | 
|  Uncollected \(< 31 days pending\)  |  ✔  |  ✔  |  The total of funds billed but not collected for less than 31 days\.  | 
|  Uncollected \(31–60 days pending\)  |  ✔  |  ✔  |  The total of funds billed but not collected for between 31–60 days\.  | 
|  Uncollected \(61–90 days pending\)  |  ✔  |  ✔  |  The total of funds billed but not collected for between 61–90 days\.  | 
|  Uncollected \(91–120 days pending\)  |  ✔  |  ✔  |  The total of funds billed but not collected for between 91–120 days\.  | 
|  Uncollected \(> 120 days pending\)  |  ✔  |  ✔  |  The total of funds billed but not collected for more than 120 days\. | 
|  Uncollected \(overall\)  |  ✔  |  ✔  |  The total of all funds billed but not collected\.  | 

## Section 5: Age of Past Due Funds<a name="age-of-past-due-funds"></a>

 This section lists data for funds that have been accrued and are payable by the customer, but have not been paid in accordance with the customer's agreement with AWS\. 


|  Column Name  |  Available for All Sellers |  Available for Sellers in the Enhanced Data Sharing Program  |  Description  | 
| --- | --- | --- | --- | 
|  Past Due \(< 31 days\)  |  ✔  |  ✔  |  The total of funds that have accrued in the last 0–31 days and are due but that the customer hasn't paid\.  | 
|  Past Due \(31–60 days\)  |  ✔  |  ✔  |  The total of funds that have accrued in the last 31–60 days and are due but that the customer hasn't paid\. | 
|  Past Due \(61–90 days\)  |  ✔  |  ✔  | The total of funds that have accrued in the last 61–90 days that are due but that the customer hasn't paid\.  | 
|  Past Due \(91–120 days\)  |  ✔  |  ✔  | The total of funds that have accrued in the last 91–120 days and are due but that the customer hasn't paid\. | 
|  Past Due \(> 120 days\)  |  ✔  |  ✔  | The total of funds that have accrued in the last 121 or more days and are due but that the customer hasn't paid\. | 
|  Past Due \(overall\)  |  ✔  |  ✔  |  The total of funds that have accrued and are due but that the customer hasn't paid\.  | 

## Section 6: Age of Disbursed Funds<a name="section-5-age-of-disbursed-funds"></a>

 This section lists data for collected funds since the previous monthly disbursement\. 


|  Column Name  |  Available for All Sellers |  Available for Sellers in the Enhanced Data Sharing Program  |  Description  | 
| --- | --- | --- | --- | 
|  Collected \(< 31 days pending\)  |  ✔  |  ✔  |  The total of funds collected that were billed in the 0–31 day range\.  | 
|  Collected \(31–60 days pending\)  |  ✔  |  ✔  |  The total of funds collected that were billed in the 31–60 day range\.  | 
|  Collected \(61–90 days pending\)  |  ✔  |  ✔  |  The total of funds collected that were billed in the 61–90 days range\.  | 
|  Collected \(91–120 days pending\)  |  ✔  |  ✔  |  The total of funds collected that were billed in the 91–120 days range\.  | 
|  Collected \(> 120 days pending\)  |  ✔  |  ✔  |  The total of funds collected that were billed in the greater than 120 days range\.  | 
|  Collected \(overall\)  |  ✔  |  ✔  |  The total of all collected funds\.  | 