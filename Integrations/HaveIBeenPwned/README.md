
# HaveIBeenPwned

Have I Been Pwned? (HIBP) is a website that allows internet users to check if their personal data has been compromised by data breaches.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|



## Actions
#### Check Account
Retrieve all breaches an account has been involved in and public "pastes" an account was found in
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"breaches": [{"PwnCount": 37217682, "IsRetired": false, "Description": "In March 2012, the music website <a href=\"https://techcrunch.com/2016/09/01/43-million-passwords-hacked-in-last-fm-breach/\" target=\"_blank\" rel=\"noopener\">Last.fm was hacked</a> and 43 million user accounts were exposed. Whilst <a href=\"http://www.last.fm/passwordsecurity\" target=\"_blank\" rel=\"noopener\">Last.fm knew of an incident back in 2012</a>, the scale of the hack was not known until the data was released publicly in September 2016. The breach included 37 million unique email addresses, usernames and passwords stored as unsalted MD5 hashes.", "DataClasses": ["Email addresses", "Passwords", "Usernames"], "IsSensitive": false, "Domain": "last.fm", "IsSpamList": false, "BreachDate": "2012-03-22", "IsFabricated": false, "ModifiedDate": "2016-09-20T20:00:49Z", "Title": "Last.fm", "Name": "Lastfm", "AddedDate": "2016-09-20T20:00:49Z", "IsVerified": true, "LogoPath": "https://haveibeenpwned.com/Content/Images/PwnedLogos/Lastfm.png"}], "pastes": [{"Date": null, "Source": "AdHocUrl", "EmailCount": 36959, "Id": "http://siph0n.in/exploits.php?id=1", "Title": "BuzzMachines.com 40k+"}]}, "Entity": "john_doe@example.com"}]
```



#### Ping
Check connectivity
Timeout - 600 Seconds









