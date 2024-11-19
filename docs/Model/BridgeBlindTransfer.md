# BridgeBlindTransfer

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel performing the blind transfer | [optional] 
**replace_channel** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel that is replacing transferer when the transferee(s) can not be transferred directly | [optional] 
**transferee** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel that is being transferred | [optional] 
**exten** | **string** | The extension transferred to | [optional] 
**context** | **string** | The context transferred to | [optional] 
**result** | **string** | The result of the transfer attempt | [optional] 
**is_external** | **bool** | Whether the transfer was externally initiated or not | [optional] 
**bridge** | [**\Swagger\Client\Model\Bridge**](Bridge.md) | The bridge being transferred | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


