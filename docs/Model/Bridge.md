# Bridge

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier for this bridge | [optional] 
**technology** | **string** | Name of the current bridging technology | [optional] 
**bridge_type** | **string** | Type of bridge technology | [optional] 
**bridge_class** | **string** | Bridging class | [optional] 
**creator** | **string** | Entity that created the bridge | [optional] 
**name** | **string** | Name the creator gave the bridge | [optional] 
**channels** | [**\Swagger\Client\Model\ListString**](ListString.md) | Ids of channels participating in this bridge | [optional] 
**video_mode** | **string** | The video mode the bridge is using. One of &#39;none&#39;, &#39;talker&#39;, &#39;sfu&#39;, or &#39;single&#39;. | [optional] 
**video_source_id** | **string** | The ID of the channel that is the source of video in this bridge, if one exists. | [optional] 
**creationtime** | [**\Swagger\Client\Model\\DateTime**](\DateTime.md) | Timestamp when bridge was created | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


