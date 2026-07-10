<p align="center">
<img src="./Copy of ActiveDirectory.png" 
     alt="Copy of ActiveDirectory" width="200"/></p>
     
# Copy of ActiveDirectory

### Description
Suspicious Active Directory activity

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationUserName|DestinationProcessName|FileName||
|SourceHostName||||Linked|SourceAddress||||
|DestinationProcessName||||Linked|FileName||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|DestinationUserName||||Linked|DestinationProcessName|FileName|||
test visual family