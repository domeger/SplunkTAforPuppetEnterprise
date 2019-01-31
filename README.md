# Splunk Add-on for Puppet Enterprise - Docs
----
- Splunk Add-on Community Supported (Puppet & Splunk Customers)
### - Requirements to Run App
- Splunk Enterprise 7.0+
- Puppet Enterprise 2018.1.1+

### - Installation Steps
----
- First generate a token from Puppet Enterprise in the shell. Make sure to take into account how long you have the token generated. We recommend to at least set it too 12 Months. We will be putting this in the Add-on Menu to help you alert when it about to expire. 
```
curl -k -X POST -H 'Content-Type: application/json' -d '{"login": "", "password": "","lifetime": "9y" }' https://$:4433/rbac-api/v1/auth/token
```

### Todos
----
 - Adding Test for TravisCI for Splunk App-Inspect

### Version History 
----
**Version 1.0**
- Includes Support for Self Signed (8081) + HTTP (8080) for PuppetDB Calls
- Rewrite of all Extraction Fields + Cleanup of Resources, Classes, and CertName
- Fixed API Key Storage
- Fixed Title to Match Pulls
- Fixed Help Text to Match Fields
- Fixed Issue with Memoryleak on Timeout API Calls

**Version 2.0**
- Support for Multiple Version of Puppet Enterprise
- Rewrite of the Factor Pull, Customer Merge Dict Feature to Only Pull certain facts. 
- Added PE Metrics for MQ
- Added Compiliation Timing
- Filter for Multiple Version of Puppet Enterprise
- Integration of VictorOps for Notification and Alerting

### License
----
[Splunk Third Party](http://docs.splunk.com/Documentation/AddonBuilder/2.2.0/UserGuide/Validate#Credit_third-party_libraries)

##### MIT License
Copyright (c) [2017] [Splunk]
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Support
----
Are you a Splunk + Puppet customer who enjoys sharing knowledge and want to put some great feature into an opensource project. We encourage you to submit issues and pull request so that we can make this Technical Addon better and help the community as a whole get better insight to their Puppet Enterprise deployments.

Feel free to leave comments or questions. We are here to make this community project more adaptive to all types of use cases.
