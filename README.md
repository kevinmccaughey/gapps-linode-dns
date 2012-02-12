#Google Apps Linode DNS Script
**Please note:** While this script was written by a Linode employee it is not endorsed nor maintained by Linode. Linode should not be contacted for support using this script or to report any bugs with the script.

**License:** This script was released under the [MIT license](http://www.opensource.org/licenses/mit-license.php).

This script aids in the creation of the MX records needed for Google Apps.  This script uses the [Linode](http://www.linode.com/?r=78a747e2c08ffb6618e260c3c62f536687b9159c) [API](http://www.linode.com/api) to create the records.  So be sure to have your API key and DomainID handy.

* Your API key can be obtained from the "My Profile" link at the top right of the Linode Manager
* If you do not know your DomainID the script will provide you with a URL to help you obtain it.

Here is the script in action:

    theckman@tron:~# ./gapps-linode-dns.sh
    ####################
    #  Google Apps MX  #
    # Records Creation #
    #      Script      #
    ####################

    This script requres you to enter your API key as well as provide the DomainID.
    If you are unsure of the DomainID this script will provide a URL you can view in
    your browser to find your DomainID.

	Enter API key: [redacted]
	
	Do you know your DomainID [y/n]: n
	
	Please visit the following URL in your web browser to obtain your DomainID:
	- https://api.linode.com/?api_key=[redacted]&api_responseformat=human&api_action=domain.list
	
	Enter your DomainID: [redacted]

    {"ERRORARRAY":[],"DATA":{"ResourceID":[redacted]},"ACTION":"domain.resource.create"}
    {"ERRORARRAY":[],"DATA":{"ResourceID":[redacted]},"ACTION":"domain.resource.create"}
    {"ERRORARRAY":[],"DATA":{"ResourceID":[redacted]},"ACTION":"domain.resource.create"}
    {"ERRORARRAY":[],"DATA":{"ResourceID":[redacted]},"ACTION":"domain.resource.create"}
    {"ERRORARRAY":[],"DATA":{"ResourceID":[redacted]},"ACTION":"domain.resource.create"}

    Should be finished at this point (assuming no errors were generated from API calls)!
    Please verify the created records within the Linode DNS Manager.
    <3 heckman

