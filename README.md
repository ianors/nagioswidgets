nagioswidgets
=============

Post installation widgets for Nagios 3.x primarily focusing on increasing the appearance (in my opinion) and usability of the mostly excellent product Nagios 3.x


Header Doohickey
=============
Header Doohickey will take advantage of the (http://nagios.sourceforge.net/docs/3_0/cgiincludes.html) Nagios custom CGI headers and footers functionality to display information about a service or host that is not easily available but extremely usefully in understanding a check.

i.e.
Check and Notification periods are 24x7 contacting admins Checks are every 5 mins. Alerts after 4 consecutive failed checks (at 1 mins interval retries) 
Command is /usr/lib/nagios/plugins/check_disk -w '20%' -c '10%' -e

The current version is something I hacked together in perl 3 years ago, I will do a new version using the crazy awesomeness of MK Livestatus (http://mathias-kettner.de/checkmk_livestatus.html).

For ease of use the configuration variables are embedded in the code.  Its currently configured for nagios on Ubuntu, just change the OBJECTS_CACHE,STATUS_DATA, RESOURCE_CFG,CGI_CFG to reflect the file locations.

Installation - simply put the common-header.ssi in the nagios ssi folder and ensure it is executable.
