Zimbra-AD-Sync
==============

Zimbra Collaboration Suite Mailboxs Active Directory Users Sync

### Installation

1. Clone this script from github or copy the files manually to your prefered directory.

2. Create settings.cfg from settings.cfg.example and change:

##### Folder settings
	    LDAPSEARCH=/opt/zimbra/bin/ldapsearch
	    ZMPROV=/opt/zimbra/bin/zmprov
	    TMP_DIR=/scripts
	    HOME_DIR=/scripts
	    EXCLUDE_FILE=exclude.txt

##### Server values
	    DOMAIN_NAME="domain.com"
	    LDAP_SERVER="ldap://dc01.domain.com"
	    BASEDN="dc=domain,dc=com"
	    BINDDN="CN=USERNAME,OU=MYOU,DC=domain,DC=com"
	    BINDPW="PASSWORD"
	    FIELDS="mail"

#### Create an AD group called Zimbra or use the filter to include the entire AD:

##### Only add members of AD group "Zimbra" in OU Users
	    #FILTER="(&(sAMAccountName=*)(objectClass=user)(givenName=*)(memberOf=cn=Zimbra,cn=Users,$BASEDN))"

##### Add all AD users
	    #FILTER="(&(sAMAccountName=*)(objectClass=user)(givenName=*))"


Author: [RaveMaker][RaveMaker].

[RaveMaker]: http://ravemaker.net
