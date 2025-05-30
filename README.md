# SKYNET
SKYNET blocklist

Update the SKYNET malware block list to this URL (I think it's option 3 in the main menu):
https://raw.githubusercontent.com/collingeorge/SKYNET/refs/heads/main/blocklist

Disable the CDN whitelisting in SKYNETs settings (I think it's option 11 in the main menu).

Leave it for 24 hours, after logging in you should see both inbound and outbound blocks. 
Outbound blocks are generally good becuase they prevent malware from reaching their command and control servers.

Credit goes to the Firehol Project (https://github.com/firehol/blocklist-ipsets/).
