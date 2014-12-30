This is no longer maintained

Where to find a list of commands
-------------------------------
You can find an up to date list of all Linode API commands at http://www.linode.com/api/ 

Using the program
----------------
Run linode_bash_api -h for help it will output the following:
```
Linode Bash API 20110619
options:
-h      Help
-v      Verbose
-F arg     Response format, default json, options wddx or human
-k arg      API Key to use
-f arg      File to get API key from, key must be the only string on the first line
-c arg      The command to run, for a list of commands see http://www.linode.com/api
-d arg      A quote string containing the data to send in "foo=bar&foo2=bar2" format
-i arg      Get data from file if  - is used get data from stdin
```
If ``-k`` or ``-f`` are ommited or don't provide an API key then the following loctions are checked
/Users/rowan/.linode_api
/etc/linode/api

Detiails of commands you can run can be found at http://www.linode.com/api/

Examples
--------

### Modify a disk of a specific linode
##### List your linodes using
``./linode_bash_api -c linode.list``
##### Get the linode ID from the returned results and run
``./linode_bash_api -c linode.disk.list -d "linodeid=<id from first step>"``
##### Get the the disk ID from the returned results and run
``./linode_bash_api -c linode.disk.update -d "linodeid=<id from second step>&diskid=<id from second step>&label=Label&isreadonly=1"``
This will set the disk label to "Label" and make the disk read only.

Contribute
----------
To contirbute to this program please feel free to fork it and submit a pull request or raise an issue.
If you feel generous and would like to donate to the project you can send money via paypal to admin {at} rwky {dot} net or flattr me at https://flattr.com/thing/319205/Linode-Bash-API
