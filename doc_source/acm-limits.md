# Quotas<a name="acm-limits"></a>

* next ACM service quotas -- apply -- / EACH AWS region / EACH AWS account
* check [ACM quotas table](https://docs.aws.amazon.com/general/latest/gr/acm.html#limits_acm) 
* if you want to request quota increases -> create a case | [AWS Support Center](https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&limitType=service-code-acm) 

## General quotas<a name="general-limits"></a>

**Topics**


****  

| Item | Default quota | 
| --- | --- | 
| maximum # of ACM expired & revoked certificates<br/> Certificates / signed by a CA from ACM Private CA do NOT count | 2500 | 
| maximum # of ACM certificates / year (== last 365 days) / region / AWS account <br/> _Example:_ if your quota is 2,500 -> you can request <= 5,000 ACM certificates / year / region & account == ONLY can have 2,500 certificates in ANY given time. if you want to request 5,000 certificates / year -> delete 2,500 during the year<br/> Certificates / signed by a CA from ACM Private CA do NOT count | 2 * your account quota | 
| # of imported certificates | 2,500 | 
| # of imported certificates / year (== last 365 days) | 2 * your account quota | 
| # of domain names / ACM certificate <br/> default quota is 10 domain names / ACM certificate<br/> first domain name / you submit -> -- included as the -- subject common name \(CN\) of the certificate <br/> ALL names -- are included in the -- Subject Alternative Name extension <br/> request <= 100 domain names <br/> [Domain names validation](acm-bestpractices.md#best-practices-validating) <br/> Certificates / 1. provided by ACM, 2. NOT imported into ACM | 10 | 
| # of Private CAsACM / -- integrated with -- ACM Private CA<br/> ways to request: 1. ACM console, 2. AWS CLI, 3. ACM API <br/> certificates -- are managed -- within the ACM environment / restrictions == public certificates / issued by ACM's restrictions <br/> [Requesting a private PKI certificate](gs-acm-request-private.md) <br/> [Issue a Private End\-Entity Certificate -- via -- ACM Private CA service](https://docs.aws.amazon.com/acm-pca/latest/userguide/PcaIssueCert.html) <br/>[if you delete a Private CA -> how does it count?](https://docs.aws.amazon.com/acm-pca/latest/userguide/PCADeleteCA.html) | 200 | 
| # of Private Certificates / CA (== lifetime) | 1,000,000 | 

## API rate quotas<a name="api-rate-limits"></a>

* next apply to the ACM API / EACH region & account
* TODO:
* ACM throttles API requests at different quotas depending on the API operation\. Throttling means that ACM rejects an otherwise valid request because the request exceeds the operation's quota for the number of requests per second\. When a request is throttled, ACM returns a `ThrottlingException` error\. The following table lists each API operation and the quota at which ACM throttles requests for that operation\. 

**Requests\-per\-second quota for each ACM API operation**


****  

| API call | Requests per second | 
| --- | --- | 
|  `AddTagsToCertificate`  |  5  | 
|  `DeleteCertificate`  |  10  | 
|  `DescribeCertificate`  |  10  | 
|  `ExportCertificate`  |  5  | 
|  `GetAccountConfiguration`  |  1  | 
| GetCertificate |  10  | 
|  `ImportCertificate`  |  1  | 
|  `ListCertificates`  |  1  | 
|  `ListTagsForCertificate`  |  10  | 
|  `PutAccountConfiguration`  |  1  | 
|  `RemoveTagsFromCertificate`  |  5  | 
| RenewCertificate |  5  | 
|  `RequestCertificate`  |  5  | 
|  `ResendValidationEmail`  |  1  | 
|  `UpdateCertificateOptions`  |  5  | 



For more information, see [AWS Certificate Manager API Reference](https://docs.aws.amazon.com/acm/latest/APIReference/)\.