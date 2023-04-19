# ZTE_router_unlock_tool

# Description
This tool can be used to unlock most **ZTE ONU/ONT routers** and obtain a completely functional root shell via telnet on port 23.  
It works by exploiting **factory_mode_auth** on ZTE routers.  
It puts the router into **telnet_factory_mode** with default factory mode credentials and obtain the randomly generated user/pass for telnet. 
# Requirements
* Python 3.7+  
* python3-pip  
* pip3 modules :
<pre>
 requests v2.28.2, pycryptodome v3.16.0, pyinstaller v5.7.0
  </pre>
# Installation
clone the repo and cd into it
```
git clone https://github.com/SahilB69/ZTE_router_unlock_tool.git
cd ZTE_router_unlock_tool
```
# Install the Requirements
```
sudo apt install python3
```
```
sudo apt install python3-pip
```
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
usage: zte_factory_mode [-h] [--user USER] [--pass PASS] [--ip IP] [--port PORT] {telnet,serial}

-h, --help            show this help message and exit  

-u, --user [USER]     username for factorymode auth (default: ['factorymode', 'CMCCAdmin', 'CUAdmin', 'telecomadmin', 'cqadmin', 'user', 'admin', 'cuadmin', 'lnadmin', 'useradmin'])  

-p, --pass [PASS]     password for factorymode auth (default: ['nE%jA@5b', 'aDm8H%MdA', 'CUAdmin', 'nE7jA%5m', 'cqunicom', '1620@CTCC', '1620@CUcc', 'admintelecom', 'cuadmin', 'lnadmin'])  
 
--ip [IP]             router ip (default: 192.168.1.1)  
 
--port [PORT]         router http port (default: 80)  
 </pre>
  
# Modes
<pre>
 [telnet,serial]       supported commands
    telnet             control telnet services on/off
    serial             control /proc/serial on/off
</pre>
# Tested Routers
  ZTE-F670L(HW v1.01), ZTE-F670L(HW v1.05), ZTE-F670L(HW v9.0)
# Notes
* serial connection mode is still experimental
