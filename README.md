# ZTE_router_unlock_tool

# Description
This tool can be used to unlock most ZTE ONU/ONT router-modem combos and obtain a root shell via telnet on port 23.
# Install Requirements
```
pip3 install -r requirements.txt
```
# Usage
Default Gateway(192.168.1.1) and built in user/pass
```
python3 zte_factory_mode.py telnet
```
Cutom args
```
python3 zte_factory_mode.py --user "USERNAME" --pass "PASSWORD" --ip "IP" --port "PORT" telnet open
```

# Options
<pre>
usage: zte_factorymode [-h] [--user USER] [--pass PASS] [--ip IP] [--port PORT] {telnet,serial}

-h, --help            show this help message and exit  

-u, --user [USER]     username for factorymode auth (default: ['factorymode', 'CMCCAdmin', 'CUAdmin', 'telecomadmin', 'cqadmin', 'user', 'admin', 'cuadmin', 'lnadmin', 'useradmin'])  

-p, --pass [PASS]     password for factorymode auth (default: ['nE%jA@5b', 'aDm8H%MdA', 'CUAdmin', 'nE7jA%5m', 'cqunicom', '1620@CTCC', '1620@CUcc', 'admintelecom', 'cuadmin', 'lnadmin'])  
 
--ip [IP]             router ip (default: 192.168.1.1)  
 
--port [PORT]         router http port (default: 80)  
 </pre>
  
# Subcommands
<pre>
 [telnet,serial]       supported commands
    telnet             control telnet services on/off
    serial             control /proc/serial on/off
</pre>
# Tested Routers
  ZTE-F670L(HW v1.01), ZTE-F670L(HW v1.05), ZTE-F670L(HW v9.0)
