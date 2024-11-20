# Channel

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier of the channel.  This is the same as the Uniqueid field in AMI. | [optional] 
**protocol_id** | **string** | Protocol id from underlying channel driver (i.e. Call-ID for chan_sip/chan_pjsip; will be empty if not applicable or not implemented by driver). | [optional] 
**name** | **string** | Name of the channel (i.e. SIP/foo-0000a7e3) | [optional] 
**state** | **string** |  | [optional] 
**caller** | [**\Swagger\Client\Model\CallerID**](CallerID.md) |  | [optional] 
**connected** | [**\Swagger\Client\Model\CallerID**](CallerID.md) |  | [optional] 
**accountcode** | **string** |  | [optional] 
**dialplan** | [**\Swagger\Client\Model\DialplanCEP**](DialplanCEP.md) | Current location in the dialplan | [optional] 
**creationtime** | [**\Swagger\Client\Model\\DateTime**](\DateTime.md) | Timestamp when channel was created | [optional] 
**language** | **string** | The default spoken language | [optional] 
**channelvars** | **object** | Channel variables | [optional] 
**caller_rdnis** | **string** | The Caller ID RDNIS | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


