# EnableThing {#reference_xkt_drz_wdb .reference}

Call this operation to enable a device that has been disabled.

## Request parameters {#section_u1b_qwm_xdb .section}

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The operation you want to perform. Set the value to EnableThing.|
|IotId|String|No| The identifier of the device that you want to disable.

 **Note:** If you use this parameter, ProductKey and DeviceName are not required. IotId is a globally unique identifier \(GUID\) of a device, and corresponds to a combination of ProductKey and DeviceName. If you specify both IotId and the combination of ProductKey and DeviceName, the system follows IotId.

 |
|ProductKey|String|No| The ProductKey of the device that you want to disable.

 **Note:** If you use this parameter, DeviceName is required.

 |
|DeviceName|String|No| The name of the device that you want to disable.

 **Note:** If you use this parameter, ProductKey is required.

 |
|Common Request Parameters|-|Yes|See [Common parameters](reseller.en-US/Developer Guide (Cloud)/API reference/Common parameters.md#).|

## Response parameters {#section_u5c_nxm_xdb .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|The globally unique ID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|
|Code|String|The error code returned when the call fails. For more information about error codes, see [Error codes](reseller.en-US/Developer Guide (Cloud)/API reference/Error codes.md#).|

## Examples {#section_ezy_5xm_xdb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=EnableThing
&IotId=SR8FiTu1R9tlUR2V1bmi0010a5****
&Public Request Parameters
```

**Response example**

-   JSON format

    ```
    {
      "RequestId":"57b144cf-09fc-4916-a272-a62902d5b207",
      "Success": true
    }
    ```

-   XML format

    ```
    <? xml version='1.0' encoding='utf-8'? >
    <EnableThingResponse>
        <RequestId>57b144cf-09fc-4916-a272-a62902d5b207</RequestId>
        <Success>true</Success>
    </EnableThingResponse>
    ```

