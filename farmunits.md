
# FarmProject Farmunits
FarmProject Farm is used as backend for Farmunits database.

Table of Contents

1. [Farm](#unit)

<a name="unit"></a>

## unit

| Specification | Value |
|-----|-----|
| Resource Path | /unit |
| API Version | 1.0.0 |
| BasePath for the API | {{.}} |
| Consumes | application/json |
| Produces |  |



### Operations


| Resource Path | Operation | Description |
|-----|-----|-----|
| /all | [GET](#GetAllUnits) | gets description of all farmunits. |
| /user | [GET](#GetUnitsByUser) | gets description of the farmunit allocated to a user. |
| /farm | [GET](#GetUnitsByFarm) | gets description of the farmunit allocated for a farm. |
| /allocate | [POST](#BuyFarmUnits) | allocate units of farm to a user. |



<a name="GetAllUnits"></a>

#### API: /all (GET)


gets description of all farmunits.



| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | array | [Unit](#github.com.georgekuruvillak.farmproject.farmunits.unit.Unit) | Success |
| 400 | object | string | Fetch farmunits failed. |


<a name="GetUnitsByUser"></a>

#### API: /user (GET)


gets description of the farmunit allocated to a user.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| userid | query | string | User id | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | array | [Unit](#github.com.georgekuruvillak.farmproject.farmunits.unit.Unit) | Success |
| 400 | object | string | Fetch farmunits failed. |


<a name="GetUnitsByFarm"></a>

#### API: /farm (GET)


gets description of the farmunit allocated for a farm.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| farmid | query | string | Farm id | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | array | [Unit](#github.com.georgekuruvillak.farmproject.farmunits.unit.Unit) | Success |
| 400 | object | string | Fetch farmunits failed. |


<a name="BuyFarmUnits"></a>

#### API: /allocate (POST)


allocate units of farm to a user.



| Param Name | Param Type | Data Type | Description | Required? |
|-----|-----|-----|-----|-----|
| userid | body | string | User id | Yes |
| userid | body | string | Farm id | Yes |
| userid | body | int | Units | Yes |


| Code | Type | Model | Message |
|-----|-----|-----|-----|
| 200 | object | [Unit](#github.com.georgekuruvillak.farmproject.farmunits.unit.Unit) | Success |
| 400 | object | string | Allocate farmunits to user failed. |




### Models

<a name="github.com.georgekuruvillak.farmproject.farmunits.unit.Unit"></a>

#### Unit

| Field Name (alphabetical) | Field Type | Description |
|-----|-----|-----|
| farmid | string |  |
| id | string |  |
| omitifempty | int |  |
| userid | string |  |


