<p align="center">
<img src="./Copy of OS.png" 
     alt="Copy of OS" width="200"/></p>
     
# Copy of OS

### Description
User activity on machine

### Rules
|Primary Source|Secondary Source|Third Source|Forth Source|Type|Primary Destination|Secondary Destination|Third Destination|Forth Destination|
|--------------|----------------|------------|------------|----|-------------------|---------------------|-----------------|-----------------|
|SourceUserName|SourceHostName|SourceAddress||Type|DestinationHostName|DestinationAddress|SourceUserName||
|DestinationHostName||||Linked|DestinationAddress||||
|SourceUserName||||Linked|SourceHostName|SourceAddress|||
|SourceHostName||||Linked|SourceAddress||||
|DestinationHostName|DestinationAddress|||Linked|FileName||||
test visual family