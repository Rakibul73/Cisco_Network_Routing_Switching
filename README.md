## Practical Lab for Academic Course CCE-416 (Network Routing and Switching Sessional)

#### Installations

* **Cisco Packet Tracer** can be downloaded from [here](https://www.netacad.com/portal/resources/packet-tracer)
<hr/>


#### `Command:`
<br/>


```bash
Router> (This is User EXEC Mode.)
Router> en
Router# (This is Privileged EXEC Mode.)
Router# config terminal
Router(config)# (This is Configuration Mode.)
Router(config)# int fa0/0
Router(config-if)#	(This is Interface level within configuration mode)
```
<hr/>

* change hostname
```bash
Router(config)# hostname HQ
HQ(config)#
```
* assing IP address to interface fa0/0 and port status on
```bash
HQ(config)#i nt fa0/0
HQ(config-if)# ip address 192.168.1.129 255.255.255.192
HQ(config-if)# no shutdown
HQ(config-if)# exit
HQ(config)#
```

* assing ip address to serial0/0/1 , port status on , set clock rate to 64000
```bash
HQ(config)# int s0/0/1
HQ(config-if)# ip address 192.168.1.229 255.255.255.252
HQ(config-if)# clock rate 64000
HQ(config-if)# no shutdown 
HQ(config-if)# exit
HQ(config)#
```


* set line console password to "cisco"
```bash
HQ(config)# line console 0
HQ(config-line)# password cisco
HQ(config-line)# login
HQ(config-line)# exit
HQ(config)#
```

* set vty password to "cisco"
```bash
HQ(config)# line vty 0
HQ(config-line)# password cisco
HQ(config-line)# login
HQ(config-line)# exit
HQ(config)#
```

* set privileged EXEC password to "cisco"
```bash
HQ(config)# enable secret class
```

* encrypt the clear text passwords.
```bash
HQ(config)# service password-encryption
```

* Require that a minimum of 10 characters be used for all passwords.
```bash
HQ(config)# security passwords min-length 10
```

* Create a banner that warns anyone accessing the device that "unauthorized access is prohibited".
```bash
HQ(config)# banner motd #Unauthorized access prohibited!#
```

* Disable DNS lookup (prevent the router from attempting to translate incorrectly entered commands as though they were hostnames.)
```bash
HQ(config)# no ip domain-lookup
```

* Set the clock on the router;
```bash
HQ# clock set 17:00:00 03 Oct 2023
```


* set ip route for network 192.168.1.0/24 , mask 255.255.255.0 , hop s0/0/0
```bash
HQ(config)# ip route 192.168.1.0 255.255.255.0 s0/0/0
```

* Save the running configuration to the startup configuration file.
```bash
HQ# copy running-config startup-config
Destination filename [startup-config]?  (Press enter)
Building configuration...
[OK]
HQ#
```


* Encrypt the clear text passwords.

  ```bash
  HQ(config)# `service password-encryption`
