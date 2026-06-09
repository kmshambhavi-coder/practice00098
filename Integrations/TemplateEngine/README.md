
# TemplateEngine

Template Engine integration provides the ability to render templates using Jinja2. Jinja2 provide fast and flexible ways to create rich templates. These templates can be used in entity insights, emails, ticketing systems, or any action that can take in a text string.
Jinja2 documentation can be found at https://jinja.palletsprojects.com/en/2.11.x/ 

Python Version - 3


#### Dependencies
| |
|-|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth-2.47.0-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|jinja2-3.1.5-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|requests-2.32.5-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|json2html-1.3.0.tar.gz|
|json2table-1.1.5-py2.py3-none-any.whl|
|protobuf-6.31.1-py3-none-any.whl|
|MarkupSafe-3.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|TIPCommon-2.3.8-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|


## Actions
#### Entity Insight
This action will use a Jinja2 template to create Entity Insights from a JSON object.  The input JSON object must be in the format of EntityResult.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|JSON Object|The raw JSON object that will be used to render the template.  |True|Content|{}|
|Template|The Jinja2 template to display.  Can be a HTML template from "Settings->Environment" or added in content box.|False|Email Content||
|Triggered By|The name of the integration that triggered this entity insight.|True|String|Siemplify|
|Remove BRs|Remove all <br> tags from the rendered template.|False|Boolean|false|
|Create Insight|When enabled, the action will create entity insights.  Default value of true.|False|Boolean|true|



##### JSON Results
```json
{"10.0.0.1": {"entity_insight": "<h1>Host Information</h1><p>IP Address: 10.0.0.1</p>", "template": "<h1>Host Information</h1><p>IP Address: {{ entity.identifier }}</p>"}}
```



#### Render Template
This action will render a Jinja2 template using a JSON input.  
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|JSON Object|The raw JSON object that will be used to render the template. This value is available as the variable input_json in the Jinja template.|False|Content|{}|
|Jinja|The Jinja template code to be rendered.  Will override Template parameter. Append |safe to disable HTML encoding.|False|Code||
|Include Case Data|When enabled, entity attributes and event data are available under the variables input_json['SiemplifyEvents'] and input_json['SiemplifyEntities']|False|Boolean|false|
|Template|The Jinja2 template to be rendered.  Can be a HTML template from "Settings->Environment" or added in content box.|False|Email Content||



##### JSON Results
```json
{"html_output": "<h1>Hello World!</h1>"}
```



#### Ping
Check connectivity
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Render Template from Array
Render Template, but for lists.  Loops through a list and applies the Jinja template to each list item.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Array input|Point to output from a previous Action that outputs an Array|False|Content|[]|
|Jinja|The Jinja template code to be rendered.  Will override Template parameter. Append |safe to disable HTML encoding.|False|Code|Start
{{ row.name }}
End|
|join|JOIN character between loops to join together|False|String|,|
|prefix|Prefix string before output|False|String|None|
|suffix|Suffix string after output|False|String|None|



##### JSON Results
```json
{"html_output": "<h1>Item 1</h1>,<h1>Item 2</h1>"}
```









