# LiveRecording

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Base name for the recording | [optional] 
**format** | **string** | Recording format (wav, gsm, etc.) | [optional] 
**target_uri** | **string** | URI for the channel or bridge being recorded | [optional] 
**state** | **string** |  | [optional] 
**duration** | [**\Swagger\Client\Model\Int**](Int.md) | Duration in seconds of the recording | [optional] 
**talking_duration** | [**\Swagger\Client\Model\Int**](Int.md) | Duration of talking, in seconds, detected in the recording. This is only available if the recording was initiated with a non-zero maxSilenceSeconds. | [optional] 
**silence_duration** | [**\Swagger\Client\Model\Int**](Int.md) | Duration of silence, in seconds, detected in the recording. This is only available if the recording was initiated with a non-zero maxSilenceSeconds. | [optional] 
**cause** | **string** | Cause for recording failure if failed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


