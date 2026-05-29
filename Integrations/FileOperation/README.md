
# FileOperation

Perform file operations and transfers.

Python Version - 3


#### Dependencies
| |
|-|
|idna-3.7-py3-none-any.whl|
|bcrypt-4.1.3-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cffi-1.16.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cryptography-42.0.5-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl|
|asn1crypto-1.5.1-py2.py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|paramiko-3.4.0-py3-none-any.whl|


## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Tarzip Files Linux
Create zip file on a remote Linux host
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|server_ip|x.x.x.x|True|String||
|username|username|True|String||
|password|password|True|Password|*****|
|source_folder|The remote server folder with the relevant files. Full path|True|String||
|file_filter|files extension to include in zip file {ex: *.txt}|True|String||
|output_folder|The remote server folder to put the zip file into|True|String||



#### Tarzip Files Windows
Compress a tarzip file on windows share
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_folder|The full path to the folder with the relevant files|False|String||
|file_filter|iles extension to include in targzip file {ex: *.txt}|False|String||
|output_folder|The path to the folder to put the zip file into|False|String||



#### Transfer File Linux To Linux
Transfer file from remote linux host to another remote linux host
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_linux_file_path|The remote server folder with the relevant files. Full path|True|String||
|source_linux_ip|x.x.x.x|True|String||
|source_linux_username|source_linux_username|True|String||
|source_linux_password|source_linux_password|True|Password|*****|
|dest_linux_path|The remote server folder to put the files into|True|String||
|dest_linux_ip|x.x.x.x|True|String||
|dest_linux_username|dest_linux_username|True|String||
|dest_linux_password|dest_linux_password|True|Password|*****|
|keep_file|Indicates weather to keep the file in source or remove it|False|Boolean||



#### Transfer File Linux To Windows
Transfer file from windows share to remote Linux host
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_linux_file_path|The remote server folder with the relevant files. Full path|True|String||
|source_linux_ip|x.x.x.x|True|String||
|source_linux_username|source_linux_username|True|String||
|source_linux_password|source_linux_password|True|Password|*****|
|dest_win_path|The server folder to put the files into|True|String||
|keep_file|Indicates weather to keep the file in source or remove it|False|Boolean||



#### Transfer File Windows To Linux
Transfer file from windows share to a remote Linux host
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_win_file_path|The server folder with the relevant files. Full path|True|String||
|dest_linux_path|The remote server folder to put the files into|True|String||
|dest_linux_ip|x.x.x.x|True|String||
|dest_linux_username|dest_linux_username|True|String||
|dest_linux_password|dest_linux_password|True|Password|*****|
|keep_file|Indicates weather to keep the file in source or remove it|False|Boolean||



#### Transfer File Windows To Windows
Transfer file between two windows shares
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_win_file_path|The folder with the relevant files. Full path|True|String||
|dest_win_path|The folder to put the files into|True|String||
|keep_file|Indicates weather to keep the file in source or remove it|True|String||



#### Zip Files Linux
Create a zip file from source folder files in a remote Linux host
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|server_ip|x.x.x.x|True|String||
|username|username|True|String||
|password|password|True|Password|*****|
|source_folder|The remote server folder with the relevant files|True|String||
|file_filter|files extension to include in zip file {ex: *.txt}|True|String||
|output_folder|The remote server folder to put the zip file into|True|String||



#### Zip Files Windows
Create a zip file from source windows share files
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|source_folder|The folder with the relevant files|True|String||
|file_filter|files extension to include in zip file {ex: *.txt}|True|String||
|output_folder|The folder to put the zip file into|True|String||









