
# GOQR

An integration for generating and reading QR codes using the qrserver.com API.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the QR Server API instance.|True|String|https://api.qrserver.com|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the server.|False|Boolean|true|


#### Dependencies
| |
|-|
|protobuf-6.33.5-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|google_auth-2.48.0-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|TIPCommon-2.2.10-py2.py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_api_python_client-2.189.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|h11-0.16.0-py3-none-any.whl|
|cryptography-46.0.4-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_api_core-2.29.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|


## Actions
#### Generate QR Code
Use the Generate QR Code action to create a QR code image from a provided string of data. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Content|The data, URL, or text string to encode into the QR code.|True|String||
|Size|The dimensions of the generated image in pixels in the format {width}x{height}. The maximum value is 1000x1000.|False|String|200x200|
|Image Format|The file format for the output image.|False|List|png|
|Error Correction|The level of data redundancy applied to the QR code. Higher levels increase damage resistance, but result in a more complex image.• Low: Recovers from up to 7% data loss.• Medium: Recovers from up to 15% data loss.• Quartile: Recovers from up to 25% data loss.• High: Recovers from up to 30% data loss.|False|List|Low|
|Margin|The width of the blank border (quiet zone) around the QR code, measured in pixels.|False|String|1|
|Foreground Color|The color of the QR code modules in R-G-B format. Default: 0-0-0 (black).|False|String|0-0-0|
|Background Color|The color of the image background in R-G-B format. Default: 255-255-255 (white).|False|String|255-255-255|



##### JSON Results
```json
{"qr_image_base64_blob": "<base64>", "size": "200x200", "format": "png", "error_correction": "Low", "margin": 1, "foreground_color": "0-0-0", "background_color": "255-255-255", "attachment_filename": "qr_code_test_com.png"}
```



#### Ping
Use the Ping action to test the connectivity to QR Server.
Timeout - 600 Seconds



#### Scan QR Code
Use the Scan QR Code action to extract and read data from a QR code image provided in Base64 format.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|QR Image Base64 Blob|The Base64-encoded string representing the QR code image file.|True|String||



##### JSON Results
```json
{"decoded_qr_codes": [{"type": "qrcode", "symbols": [{"seq": 0, "data": "This is the decoded text from the QR code.", "error": null}]}]}
```









