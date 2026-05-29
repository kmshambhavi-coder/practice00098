
# ApacheKafka

Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Kafka Brokers|A comma-separated list of Kafka brokers to connect to, in the format `hostname:port`.|True|String||
|Use TLS for connection|If enabled, the integration uses TLS encryption for authentication. A CA certificate is mandatory for this connection.|False|Boolean|false|
|Use SASL PLAIN with TLS for connection|If enabled, the integration uses the SASL PLAIN username and password mechanism for authentication. This option requires a SASL Username and Password to be provided. It is only supported with TLS encryption, which requires a CA certificate.|False|Boolean|false|
|CA certificate of Kafka server|The Certificate Authority (CA) certificate used to verify the identity of the Kafka server.|False|Password|*****|
|Client certificate|The client's certificate for mutual TLS authentication with the Kafka server.|False|Password|*****|
|Client certificate key|The private key that corresponds to the client's certificate, used for mutual TLS authentication.|False|Password|*****|
|Client certificate key password|The password used to decrypt the client certificate's private key.|False|Password|*****|
|SASL PLAIN Username|The username for SASL PLAIN authentication with Kafka brokers.|False|String||
|SASL PLAIN Password|The password for SASL PLAIN authentication with Kafka brokers.|False|Password|*****|


#### Dependencies
| |
|-|
|requests-2.32.4-py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|protobuf-6.31.1-cp39-abi3-manylinux2014_x86_64.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|typing_extensions-4.14.1-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|TIPCommon-2.2.9-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|confluent_kafka-2.11.0-cp311-cp311-manylinux_2_28_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|google_api_python_client-2.177.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|certifi-2025.7.14-py3-none-any.whl|


## Actions
#### Ping
Use the Ping action to test the connectivity to Apache Kafka.
Timeout - 600 Seconds









## Connectors
#### Apache Kafka - Messages Connector
The Apache Kafka Connector retrieves messages from Apache Kafka.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The name of the field that stores the product name.|True|String|Product Name|
|EventClassId|The name of the field that determines the event name.|True|String|event_type|
|Environment Field Name|The name of the field that stores the environment name.If the field is not found, the system uses the default environment. |False|String||
|Environment Regex Pattern|A regular expression pattern that runs on the value from the Environment Field Name field to manipulate the result.The default value, .*, retrieves the raw field value.If the regular expression pattern is empty or the environment value is null, the system uses the default environment.|False|String|.*|
|PythonProcessTimeout|The timeout, in seconds, for the Python process running the script.|True|Integer|180|
|Kafka Brokers|A comma-separated list of Kafka brokers to connect to, in the format `hostname:port`.|True|String||
|Use TLS for connection|If enabled, the integration uses TLS encryption for authentication. A CA certificate is mandatory for this connection.|False|Boolean|false|
|Use SASL PLAIN with TLS for connection|If enabled, the integration uses the SASL PLAIN username and password mechanism for authentication. This option requires a SASL Username and Password to be provided. It is only supported with TLS encryption, which requires a CA certificate.|False|Boolean|false|
|CA certificate of Kafka server|The Certificate Authority (CA) certificate used to verify the identity of the Kafka server.|False|Password|*****|
|Client certificate|The client's certificate for mutual TLS authentication with the Kafka server.|False|Password|*****|
|Client certificate key|The private key that corresponds to the client's certificate, used for mutual TLS authentication.|False|Password|*****|
|Client certificate key password|The password used to decrypt the client certificate's private key.|False|Password|*****|
|SASL PLAIN Username|The username for SASL PLAIN authentication with Kafka brokers.|False|String||
|SASL PLAIN Password|The password for SASL PLAIN authentication with Kafka brokers.|False|Password|*****|
|Topic|The Kafka topic from which incidents are retrieved.|True|String||
|Consumer group ID|The identifier of the consumer group used when retrieving incidents.|False|String||
|Partitions|A CSV list of partitions from which to fetch messages.|False|String||
|Initial Offset|The initial offset specifies where the connector starts fetching messages.A positive integer fetches from that offset number. To start from the beginning or end of the partition, use the values 'earliest' or 'latest'.|False|String||
|Max Messages To Fetch|The maximum number of messages the connector processes per iteration.|True|Integer|100|
|Poll Timeout|Poll timeout to consume a message from Kafka, in seconds.|False|Integer|5|
|Case Name Template|A custom case name.You can use placeholders in the format [field_name], for example: Phishing - [event_mailbox].This parameter adds a custom_case_name key to the Google SecOps event.The connector extracts placeholder values from the first Google SecOps event, and placeholders are only supported for fields that contain a string value.|False|String||
|Alert Name Template|A custom alert name.You can use placeholders in the format [field_name], for example: Phishing - [event_mailbox].The connector extracts placeholder values from the first Google SecOps event, and placeholders are only supported for fields that contain a string value.If you do not provide a value or use an invalid template, the connector uses the fallback value "{Connector name} - Alert".|True|String||
|Rule Generator Template|A custom rule generator.You can use placeholders in the format [field_name], for example: Phishing - [event_mailbox].The connector extracts placeholder values from the first Google SecOps event, and placeholders are only supported for fields that contain a string value.If you do not provide a value or use an invalid template, the connector uses the fallback value "{Connector name} - Rule Generator".|True|String||
|Timestamp Field|The name of the field that contains the Google SecOps alert timestamp.If the timestamp is not in Unix epoch format, its format must be defined in the Timestamp Format parameter.|True|String|timestamp|
|Timestamp Format|The format of the message timestamp.The connector requires this format to process messages correctly.If the timestamp is not in Unix epoch format and a timestamp format is not configured, the connector will fail.|False|String|%Y-%m-%dT%H:%M:%S.%fZ|
|Severity Mapping JSON|The JSON object used by the connector to extract the severity level from the message.|True|String|{"Default": 60}|
|Unique ID Field|The name of the field that provides a unique message identifier. If a value is not set, the connector generates and uses a SHA-256 hash as the message identifier.|False|String||
|Disable Overflow|If enabled, the connector ignores the Google SecOps overflow mechanism when creating alerts.|False|Boolean|true|
|Verify SSL|If enabled, the integration validates the SSL certificate for the Apache Kafka connection.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server.|False|String||
|Proxy Username|The username for proxy authentication.|False|String||
|Proxy Password|The password for proxy authentication.|False|Password|*****|




