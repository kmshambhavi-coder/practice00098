
# ArcannaAI

Arcanna.ai is a platform for delivering decision intelligence. It augments Security Operation Center analysts in dealing with incoming threats by increasing analyst efficiency in decision-making.

Arcanna.ai continuously learns from cybersecurity experts by using an innovative method for expert knowledge integration into deep neural nets by combining a continuous human feedback-loop, Natural Language Processing and deep learning.

Our platform enables SOC Analyst decisions to be augmented using AI models obtained by encoding knowledge from the existing processes across the entire security team and uses it to predict future decisions, increasing efficiency in decision-making.

More information is available at https://arcanna.ai


Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Url||True|String|https://your-arcanna.url|
|Api Key||True|Password|*****|
|SSL Verification||False|Boolean|false|


#### Dependencies
| |
|-|
|requests-2.32.4-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|


## Actions
#### Export full event

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Where to fetch event|True|String| |
|Event ID|Event ID To fetch|True|String| |



##### JSON Results
```json
{"event_id": " 32072928741742", "ingest_timestamp": "2024-05-30T07:21:46.292874Z", "status": "OK", "arcanna_event": {"id": "32072928741742", "metadata": {"severity": 0, "ingested_timestamp": "2024-05-30T07:21:46.292874Z", "id": "32072928741742", "description": "NEW_USER_CMD_LINE_WINDOWSA484EC16-379B-432E-B960-8DF24A381054"}, "arcanna": {"result": "class_2", "result_label": "Medium", "inference_status": "finished", "bucket_state": null, "original_id": "32072928741742", "original_index": "", "artifacts": [], "log_messages": [{"component": "Input", "level": "info", "component_subcategory": "Undefined", "content": "Read from Undefined", "timestamp": "2024-05-30T07:21:55.939337+00:00"}, {"component": "Inference", "level": "warn", "component_subcategory": "Generic", "content": "Skip record because it is incompatible with selected features.", "timestamp": "2024-05-30T07:21:58.445649+00:00"}, {"component": "Output", "level": "info", "component_subcategory": "Elasticsearch", "content": "Writing to Elasticsearch", "timestamp": "2024-05-30T07:21:59.218356+00:00"}], "timers": {"output": {"per_alert_in_batch_ms": 30.0, "total_ms": 30, "start": 1717053719188, "end": 1717053719218, "kafka_overhead_in_ms": 741}, "core": {"end": 1717053715939}, "total_kafka_overhead_in_s": 1.714, "inference": {"per_alert_in_batch_ms": 1535.0, "total_ms": 1535, "start": 1717053716912, "end": 1717053718447, "kafka_overhead_in_ms": 973}, "total_pipeline_in_s": 3.279}, "batch_uuid": "f652b157-8ebb-4434-9d07-25d69f423f65", "inference_result": "no_decision", "model": {"path": "generic-1-3207-model-1716805470.hdf5", "timestamp": "2024-05-27T10:24:30"}, "batch_master_uuid": "ba66e308-6e8a-4888-8b65-42cc3fa31f0f", "bucket_id": "FNTUqupSidwDGFaAd3YpZW", "features_hash": "9c13e5586414e5b2ba64874931a1653e912e63375256ea01f02b8d000d70bb5b", "key_hash": "57e5c9981b303223cfd55d99cda6ae5a87be1a58ec829dc3d47f9445a808a08c", "full_hash": "57e5c9981b303223cfd55d99cda6ae5a87be1a58ec829dc3d47f9445a808a08c9c13e5586414e5b2ba64874931a1653e912e63375256ea01f02b8d000d70bb5b", "confidence_score": 49.71}, "@timestamp": "2024-05-30T07:21:46.292874Z", "timestamp_inference": "2024-05-30T07:21:58.443060+00:00"}}
```



#### Get AI Job by name

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job name|Job name for which the job details should be fetched |True|String| |



##### JSON Results
```json
{"job_id": 3207, "title": "Arcanna Accenture Demo Calin Exposer", "status": "ENABLED", "retrain_state": "RETRAIN_FINISHED", "retrain_msg": "Retraining finished successfully", "labels": ["Low", "Medium", "High", "Critical", "Informational"], "features": ["preserve_original_id", "additional_properties.AlertGroupIdentifier", "additional_properties.detection_1_ruleLabels_1_value", "additional_properties.detection_1_ruleLabels_2_value", "additional_properties.detection_1_ruleLabels_4_key", "additional_properties.detection_1_ruleType", "additional_properties.event_target_process_file_fullPath", "source_host_name", "source_nt_domain", "source_process_name", "source_user_name"], "processed_documents_count": 50, "feedback_documents_count": 10, "last_processed_timestamp": "2024-05-30T07:21:59.391204+00:00", "last_feedback_timestamp": "2024-08-13T09:47:21.605603+00:00", "last_train_start_timestamp": "2024-05-27T10:24:35.382371+00:00", "last_train_finished_timestamp": "2024-05-27T10:24:50.067615+00:00", "invalid": false}
```



#### Get AI Job decision set

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID for which decision set should be fetched |True|String| |



##### JSON Results
```json
["Low", "Medium", "High", "Critical", "Informative"]
```



#### Get AI Job decision set by job name

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job name|Job name for which decision set should be fetched |True|String| |



##### JSON Results
```json
["Low", "Medium", "High", "Critical", "Informative"]
```



#### Get Arcanna decision

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job Id|Arcanna Job id|True|String||
|Event Id|Arcanna Event ID|True|String||
|Retry count|How many times request should be re-tried|True|String|20|
|Seconds per retry|How many seconds should wait between requests|True|String|5|



##### JSON Results
```json
{"event_id": "3207204311332", "ingest_timestamp": "2024-05-30T07:06:02.020431Z", "status": "OK", "result": "class_1", "result_label": "Escalate", "error_message": "", "bucket_state": "new", "outlier": false, "confidence_score": 86.43}
```



#### Get Jobs
Retrieves Arcanna.AI available jobs  and saves the results
Timeout - 600 Seconds



##### JSON Results
```json
[{"job_id": 3207, "title": "Arcanna Demo Job", "status": "ENABLED", "retrain_state": null, "retrain_msg": null, "labels": ["Low", "Medium", "High", "Critical", "Informative"], "features": ["additional_properties.detection_1_ruleLabels_1_value", "additional_properties.detection_1_ruleLabels_2_value", "additional_properties.detection_1_ruleLabels_4_key", "additional_properties.detection_1_ruleType", "source_host_name", "source_nt_domain", "source_process_name", "source_user_name"], "processed_documents_count": 4, "feedback_documents_count": 0, "last_processed_timestamp": "2024-05-27T09:00:15.779399+00:00", "last_feedback_timestamp": "2024-05-27T08:59:53.839953+00:00", "last_train_start_timestamp": null, "last_train_finished_timestamp": null, "invalid": false}]
```



#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Send Active Alert from Case to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Alert identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the alert. Default value for Google SecOps Alerts is "identifier".|False|String|identifier|
|Use Alert ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the alert.If True, Arcanna uses the id found in the "Alert identifier field".|False|Boolean|false|



##### JSON Results
```json
{"event_id": "12223273231449", "job_id": 1222, "ingest_timestamp": "2024-08-07T14:38:43.327323Z", "status": "pending_inference", "error_message": ""}
```



#### Send Analyst Feedback to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Id|Arcanna Event id|True|String||
|Username|Analyst name who uses this action|True|Users|Admin|
|Job Id|Arcanna Job Id|True|String||
|Analyst Feedback|A string representing the feedback an analyst provides on an event.|True|String|_|



##### JSON Results
```json
{"status": "updated"}
```



#### Send Case to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the case. Default value for Google SecOps Cases is "identifier".|False|String|identifier|
|Use case ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the case.If True, Arcanna uses the id found in the "Case identifier field".|False|Boolean|false|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |



##### JSON Results
```json
{"event_id": "12223273231449", "job_id": 1222, "ingest_timestamp": "2024-08-07T14:38:43.327323Z", "status": "pending_inference", "error_message": ""}
```



#### Send event to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Username|Username registered for audit purposes|True|Users|@Administrator|
|Event ID mapping field|Field that will be used as reference ID with Arcanna.ai|False|String|None|
|Send individual alerts from case|Send individual alerts or full case to Arcanna.ai|False|Boolean|false|



##### JSON Results
```json
{}
```



#### Send JSON Document to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the document. The field supports dot notation field names such as 'doc.id'.|False|String||
|Use document ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the document.If True, Arcanna uses the id found in the "Identifier field".|False|Boolean|false|
|JSON Document|The JSON document to be sent to Arcanna.|True|Code|{}|



##### JSON Results
```json
{"event_id": "12223273231449", "job_id": 1222, "ingest_timestamp": "2024-08-07T14:38:43.327323Z", "status": "pending_inference", "error_message": ""}
```



#### Trigger AI Model training

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|ID For job where training will be triggered|True|String||
|Username|Username for audit|True|Users|@Administrator|



##### JSON Results
```json
{"status": "OK", "error_message": ""}
```



#### Update alert priority
Change the alert priority based on the input.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Priority|Choose the new priority. Must be one the following values:- Informative- Low- Medium- High- Critical|True|String|[ArcannaAI_Get Arcanna decision_1.JsonResult| "result_label"]|



##### JSON Results
```json
{}
```









