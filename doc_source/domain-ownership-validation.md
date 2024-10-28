# Validating domain ownership<a name="domain-ownership-validation"></a>

* ways that ACM -- validates that -- you own or control ALL domain names / you specify | your request | 👀before Amazon CA issue a certificate 👀
  * [DNS validation](dns-validation.md)
    * 👀recommended one 👀
      * Reasons
        * if you use Amazon Route 53 to manage your public DNS records -> you can update your records -- through -- ACM
        * if certificate remains in use & DNS record is in place -> ACM -- automatically renews -- DNS-validated certificates
  * [email validation](email-validation.md) 
    * use cases
      * if you lack authorization to edit your domain's DNS database
    * requirements
      * action by the domain owner / ACM -- begins sending -- renewal notices 45 days before expiration

* Validation
  * ⚠️ONLY | publicly trusted certificates / -- issued by -- ACM ⚠️
    * == ACM does NOT validate domain ownership for
      * [imported certificates](import-certificate.md) or
      * certificates / -- signed by a -- private CA
