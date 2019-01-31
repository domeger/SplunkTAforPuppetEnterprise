# Splunk Add-on for Puppet Enterprise

## Requirements to run this add-on

- Splunk Enterprise 7.0+
- Puppet Enterprise 2018.1.1+
- Splunk App for Puppet Enterprise (Obtain from [Github](https://github.com/puppetlabs/SplunkAppforPuppetEnterprise/)) — _This component visualises data from Puppet Enterprise collected and stored in Splunk by this add-on._

## Installation Steps

1. First generate a token from Puppet Enterprise in the shell. Make sure to take into account how long you have the token generated. We recommend to at least set it too 12 Months. We will be putting this in the Add-on Menu to help you alert when it about to expire. 

```shell
curl -k -X POST -H 'Content-Type: application/json' -d '{"login": "", "password": "","lifetime": "9y" }' https://$:4433/rbac-api/v1/auth/token
```

## Version history

### Version 2.0

- Support for Multiple Version of Puppet Enterprise
- Rewrite of the Factor Pull, Customer Merge Dict Feature to Only Pull certain facts.
- Added PE Metrics for MQ
- Added Compiliation Timing
- Filter for Multiple Version of Puppet Enterprise
- Integration of VictorOps for Notification and Alerting

### Version 1.0

- Includes Support for Self Signed (8081) + HTTP (8080) for PuppetDB Calls
- Rewrite of all Extraction Fields + Cleanup of Resources, Classes, and CertName
- Fixed API Key Storage
- Fixed Title to Match Pulls
- Fixed Help Text to Match Fields
- Fixed Issue with Memoryleak on Timeout API Calls

## Support

Are you a Splunk + Puppet customer who enjoys sharing knowledge and want to put some great features into an open-source project. We encourage you to [submit issues](https://github.com/puppetlabs/SplunkAppforPuppetEnterprise/issues/new) and pull requests so that we can make this Technical Addon better and help the community as a whole get better insight to their Puppet Enterprise deployments.

Feel free to leave comments or questions. We are here to make this community project more adaptive to all types of use cases.
