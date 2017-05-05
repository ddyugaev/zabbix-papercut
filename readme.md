# Papercut template for Zabbix

**Tested on**
* Zabbix 3.2.4  
* [Python 2.7.13 for Windows](https://www.python.org/downloads/windows/)  
* Papercut 17.07

**Steps**

1.	Install the Zabbix agent on the Papercut server;

2.  Copy paste content from zabbix_agentd.d/userparameter_papercut.conf to zabbix agent config file;

3.	Copy whole folder "scripts" to Zabbix agent folder on Papercut server

```C:\Program Files\Zabbix Agent\
```

4.	Edit the papercut.conf file and add the correct Authorization token and papercut server ip.  
You can get your unique authorization key under ‘**Options > Advanced**’ in Papercut web admin interface;

5.	Restart the Zabbix-Agent to apply new new configuration;

6.	From the folder “template” import zabbix_papercut_template.xml template in Zabbix (Configuration -- Templates –- Import);

7.  Open ZBX-Papercut template in Zabbix and edit 2 macros in Macros tab (Configuration –- Templates –- ZBX-papercut –- Macros). Same as Step 4.  
Exemple:  
{$AUTHORIZATION} = (Authorization=oTKVWmrG6nkPbcdeDjcdmEmLPV)  
{$PAPERCUTIP} => papercut server IP (10.10.10.1);

8. Create host (Configuration -- Host -- Create host) and apply template to it;

9.	Check the latest data page to see if it works.
