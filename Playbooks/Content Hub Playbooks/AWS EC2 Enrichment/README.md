# AWS EC2 Enrichment
This block retrieves EC2 instance data associated with the case and provides context for other actions or analysis.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False


##### Input Parameters
|Name|Default Value|
|----|-------------|


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Instance Ids|This action includes basic Pythonic string functions as mentioned below - Lower: Converts the input string to lowercase.Upper: Converts the input string to uppercase (duplicated case in the script).Strip: Removes leading and trailing whitespaces from the input string.Title: Converts the first character of each word in the input string to uppercase.Count: Counts the occurrences of `param_1` in the input string.Replace: Replaces occurrences of `param_1` with `param_2` in the input string.Find: Finds the first occurrence of `param_1` in the input string and returns its index.IsAlpha: Checks if all characters in the input string are alphanumeric.IsDigit: Checks if all characters in the input string are digits.Regex Replace: Performs a regex-based replacement of `param_1` with `param_2` in the input string.JSON Serialize: Converts the input string to a JSON formatted string.Regex: Finds all occurrences of the pattern `param_1` in the input string, joins them using `param_2` (defaulting to ", "), and returns the result.DecodeBase64: Decodes the input string from base64 using `param_1` as the encoding type. Default to utf-8EncodeBase64: Encodes the input string in base64 using `param_1` as the encoding type. Default to utf-8RemoveNewLines: Removes new lines from the input string, replacing them with spaces.Split: Splits the input string using `param_1` (or "," if not provided) and adds the result to the Siemplify result.|Functions|String Functions|
|List Security Groups|Describes the specified security groups or all of your security groups. A security group is for use with instances either in the EC2-Classic platform or in a specific VPC. For more information, see https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html|AWSEC2|List Security Groups|
|List Instances - EC2|Describes the specified instances or all instances.|AWSEC2|List Instances|

Readme addon