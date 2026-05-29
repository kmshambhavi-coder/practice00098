
# Imgbb

Imgbb is a free image hosting and sharing service.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|API Key|True|Password|*****|
|Verify SSL|Verify Proxy|False|Boolean|true|


#### Dependencies
| |
|-|
|requests-2.32.4-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|


## Actions
#### Ping
Test connectivity with Imgbb
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Upload Image From Base64
Upload base64 to Imgbb ( the outcome is the image URL)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Image in base64|The base64 of the image you would like to upload to Imgbb|True|String| |



##### JSON Results
```json
{"data": {"id": "Ln3jtww", "title": "80e65c37e8d2", "url_viewer": "https://ibb.co/Ln3tww", "url": "https://i.ibb.co/2qMWcc/80e65c37e8d2.png", "display_url": "https://i.ibb.co/MMmwTT/80e6c37e8d2.png", "size": 52056, "time": "1600338508", "expiration": "600", "image": {"filename": "80e65ce8d2.png", "name": "80e65c37e8d2", "mime": "image/png", "extension": "png", "url": "https://i.ibb.co/72qWcc/80e657e8d2.png"}, "thumb": {"filename": "80e65c37e8d2.png", "name": "80e65c37e8d2", "mime": "image/png", "extension": "png", "url": "https://i.ib.co/Ln3jtww/80ec37ed2.png"}, "medium": {"filename": "80e637e8d2.png", "name": "80e65c38d2", "mime": "image/png", "extension": "png", "url": "https://i.ibb.co/MMwVTT/80ec37e8d2.png"}, "delete_url": "https://ibb.co/Ln3jw/ef3fed8a0e9b987a04a25e86ef8bd9"}, "success": true, "status": 200}
```



#### Upload Image From File Path
Upload image from file path to Imgbb ( the outcome is the image URL)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Image File Path|The file path of the image you would like to upload to Imgbb|True|String||



##### JSON Results
```json
{"data": {"id": "TgSJ5m1", "title": "08cdb41c98bf", "url_viewer": "https://ibb.co/Tg5m1", "url": "https://i.ibb.co/1m5Bx8M/08c41c98bf.jpg", "display_url": "https://i.ibb.co/1m5Bx8M/08cdbc98bf.jpg", "size": 5520, "time": "1600338870", "expiration": "600", "image": {"filename": "08cdb41c98bf.jpg", "name": "08cdb41c98bf", "mime": "image/jpeg", "extension": "jpg", "url": "https://i.ibb.co/1m5Bx8M/08c41c98bf.jpg"}, "thumb": {"filename": "08cdb41c98bf.jpg", "name": "08cdb41c98bf", "mime": "image/jpeg", "extension": "jpg", "url": "https://i.ibb.co/TgSJ5m1/08cdb41c98bf.jpg"}, "delete_url": "https://ibb.co/TgSJ5m1/06651ef6cec6909c85af7d18409c39"}, "success": true, "status": 200}
```









