# What Is AWS Certificate Manager?<a name="acm-overview"></a>

* ACM
  * handles the complexity about public and private SSL/TLS X.509 certificates, of
    * creating,
    * storing,
    * renewing,
    * importing
    * [exporting](export-private.md)
      * -> can be used | ALL your internal PKI
  * ACM wildcard certificates
    * allows
      * protecting unlimited # of subdomains
* uses of SSL/TLS X.509 certificates 
  * protect
    * your AWS
      * websites
      * applications
    * domain names
      * 1!
      * multiple
      * wildcard
      * combinations of
* ways to provide certificates -- for -- your [integrated AWS services](acm-services.md)
  * issuing them directly -- via -- ACM or
  * [importing](import-certificate.md) TP certificates | ACM management system 

## Is ACM the right service for me?<a name="service-options"></a>

* ways to manage X.509 certificates
  1. **AWS Certificate Manager \(ACM\)**
     1. use cases
        1. enterprise customers / need 
           1. to secure -- via -- TLS
           2. significant traffic requirements
        2. security management / automate the renewal of expiring certificates 
     2. ACM certificates -- are deployed through --
        1.Elastic Load Balancing
        2. Amazon CloudFront, 
        3. Amazon API Gateway,
        4. other [integrated AWS services](acm-services.md)
  2. **ACM Private CA**
     1. use cases
        1. enterprise customers / build a public key infrastructure \(PKI\) | AWS cloud & use | the organization
     2. allows
        1. creating your own certificate authority \(CA\) hierarchy
        2. issuing certificates -- for authenticating -- users, computers, applications, services, servers, and other devices
           1. these certificates can NOT be used | internet
     3. see the [ACM Private CA User Guide](https://docs.aws.amazon.com/acm-pca/latest/userguide/PcaWelcome.html)

**Topics**

* [Concepts](acm-concepts.md)
* [ACM certificate characteristics](acm-certificate.md)
* [Supported Regions](acm-regions.md)
*[Services integrated with AWS Certificate Manager](acm-services.md)
* [Site seals and trust logos](acm-siteseal.md)
* [API rate quotas](acm-limits.md#api-rate-limits)
* [Best practices](acm-bestpractices.md)
* [Pricing for AWS Certificate Manager](acm-billing.md)