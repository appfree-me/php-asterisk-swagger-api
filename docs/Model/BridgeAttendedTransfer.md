# BridgeAttendedTransfer

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transferer_first_leg** | [**\Swagger\Client\Model\Channel**](Channel.md) | First leg of the transferer | [optional] 
**transferer_second_leg** | [**\Swagger\Client\Model\Channel**](Channel.md) | Second leg of the transferer | [optional] 
**replace_channel** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel that is replacing transferer_first_leg in the swap | [optional] 
**transferee** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel that is being transferred | [optional] 
**transfer_target** | [**\Swagger\Client\Model\Channel**](Channel.md) | The channel that is being transferred to | [optional] 
**result** | **string** | The result of the transfer attempt | [optional] 
**is_external** | **bool** | Whether the transfer was externally initiated or not | [optional] 
**transferer_first_leg_bridge** | [**\Swagger\Client\Model\Bridge**](Bridge.md) | Bridge the transferer first leg is in | [optional] 
**transferer_second_leg_bridge** | [**\Swagger\Client\Model\Bridge**](Bridge.md) | Bridge the transferer second leg is in | [optional] 
**destination_type** | **string** | How the transfer was accomplished | [optional] 
**destination_bridge** | **string** | Bridge that survived the merge result | [optional] 
**destination_application** | **string** | Application that has been transferred into | [optional] 
**destination_link_first_leg** | [**\Swagger\Client\Model\Channel**](Channel.md) | First leg of a link transfer result | [optional] 
**destination_link_second_leg** | [**\Swagger\Client\Model\Channel**](Channel.md) | Second leg of a link transfer result | [optional] 
**destination_threeway_channel** | [**\Swagger\Client\Model\Channel**](Channel.md) | Transferer channel that survived the threeway result | [optional] 
**destination_threeway_bridge** | [**\Swagger\Client\Model\Bridge**](Bridge.md) | Bridge that survived the threeway result | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


