
# FarmProject Farm
FarmProject Farm is used as backend for Farm database.

Table of Contents

1. [Farm](#farm)

<a name="farm"></a>

## farm

| Specification | Value |
|-----|-----|
| Resource Path | /farm |
| API Version | 1.0.0 |
| BasePath for the API | {{.}} |
| Consumes | application/json |
| Produces |  |



### Operations


| Resource Path | Operation | Description |
|-----|-----|-----|
| /create | [POST](#CreateFarm) | creates a new farm. |
| /farm | [GET](#GetFarm) | gets description of the farm. |
| /all | [GET](#GetAllFarms) | gets description of all farms. |
| /deactivate | [POST](#DeactivateFarm) | deactivates the farm. |
| /update | [POST](#UpdateFarm) | updates the information of the farm. |



<a name="CreateFarm"></a>

#### API: /create (POST)


creates a new farm.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| farm | body | [Farm](#github.com.georgekuruvillak.farmproject.farms.farm.Farm) | Farm Information | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | object | string | Success |
| 400 | object | string | Farm creation failed. |


<a name="GetFarm"></a>

#### API: /farm (GET)


gets description of the farm.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| id | query | string | Farm id | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | object | [Farm](#github.com.georgekuruvillak.farmproject.farms.farm.Farm) | Success |
| 400 | object | string | Fetch user failed. |


<a name="GetAllFarms"></a>

#### API: /all (GET)


gets description of all farms.



| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | array | [Farm](#github.com.georgekuruvillak.farmproject.farms.farm.Farm) | Success |
| 400 | object | string | Fetch farm failed. |


<a name="DeactivateFarm"></a>

#### API: /deactivate (POST)


deactivates the farm.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| id | query | string | Farm ID | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | object | string | Success |
| 400 | object | string | Deactivate farm failed. |


<a name="UpdateFarm"></a>

#### API: /update (POST)


updates the information of the farm.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| id | query | string | Farm ID | Yes |
| farm | body | [Farm](#github.com.georgekuruvillak.farmproject.farms.farm.Farm) | Farm Information | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | object | string | Success |
| 400 | object | string | Deactivate user failed. |




### Models

<a name="github.com.georgekuruvillak.farmproject.farms.farm.Farm"></a>

#### Farm

| Field Name (alphabetical) | Field Type | Description |
|-----|-----|-----|
|  boolean | bool |  |
| description | string |  |
| harvest | int |  |
| id | string |  |
| images | array |  |
| insurance | string |  |
| name | string |  |
| period | int |  |
| return | float32 |  |
| size | int |  |
| unitprice | float32 |  |
| units | int |  |


