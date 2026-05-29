
# JuniperVSRX

vSRX is a virtual security appliance that provides security and networking services at the perimeter or edge in virtualized private or public cloud environments. vSRX runs as a virtual machine (VM) on a standard x86 server. vSRX is built on the Junos operating system (Junos OS) and delivers networking and security features similar to those available on the software releases for the SRX Series Services Gateways. The vSRX provides you with a complete Next-Generation Firewall (NGFW) solution, including core firewall, VPN, NAT, advanced Layer 4 through Layer 7 security services such as Application Security, intrusion detection and prevention (IPS), and UTM features including Enhanced Web Filtering and Anti-Virus. Combined with Sky ATP, the vSRX offers a cloud-based advanced anti-malware service with dynamic analysis to protect against sophisticated malware, and provides built-in machine learning to improve verdict efficacy and decrease time to remediation.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address||True|IP|x.x.x.x|
|Port||True|Integer|8080|
|Username||True|String||
|Password||True|Password|*****|


#### Dependencies
| |
|-|
|markupsafe-3.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|pyserial-3.5-py2.py3-none-any.whl|
|ncclient-0.7.1-py3-none-any.whl|
|junos_eznc-2.7.1-py3-none-any.whl|
|cryptography-46.0.5-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|transitions-0.9.3-py2.py3-none-any.whl|
|yamlordereddictloader-0.4.2-py3-none-any.whl|
|jinja2-3.1.6-py3-none-any.whl|
|pyyaml-6.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|invoke-2.2.1-py3-none-any.whl|
|scp-0.15.0-py2.py3-none-any.whl|
|bcrypt-5.0.0-cp39-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|lxml-6.0.2-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pynacl-1.6.2-cp38-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|paramiko-4.0.0-py3-none-any.whl|


## Actions
#### Add IP To Address Set
Add IP address to an address set.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address Set Name|Address Set Name|True|String|None|
|Zone Name|Zone Name|False|String|None|



#### Ping
Test integration connectivity.
Timeout - 600 Seconds



#### Remove IP From Address Set
Remove IP address from address set.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address Set Name|Address Set Name|True|String|None|
|Zone Name|Zone Name|False|String|None|









