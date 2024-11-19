# RTPstat

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**txcount** | [**\Swagger\Client\Model\Int**](Int.md) | Number of packets transmitted. | [optional] 
**rxcount** | [**\Swagger\Client\Model\Int**](Int.md) | Number of packets received. | [optional] 
**txjitter** | **double** | Jitter on transmitted packets. | [optional] 
**rxjitter** | **double** | Jitter on received packets. | [optional] 
**remote_maxjitter** | **double** | Maximum jitter on remote side. | [optional] 
**remote_minjitter** | **double** | Minimum jitter on remote side. | [optional] 
**remote_normdevjitter** | **double** | Average jitter on remote side. | [optional] 
**remote_stdevjitter** | **double** | Standard deviation jitter on remote side. | [optional] 
**local_maxjitter** | **double** | Maximum jitter on local side. | [optional] 
**local_minjitter** | **double** | Minimum jitter on local side. | [optional] 
**local_normdevjitter** | **double** | Average jitter on local side. | [optional] 
**local_stdevjitter** | **double** | Standard deviation jitter on local side. | [optional] 
**txploss** | [**\Swagger\Client\Model\Int**](Int.md) | Number of transmitted packets lost. | [optional] 
**rxploss** | [**\Swagger\Client\Model\Int**](Int.md) | Number of received packets lost. | [optional] 
**remote_maxrxploss** | **double** | Maximum number of packets lost on remote side. | [optional] 
**remote_minrxploss** | **double** | Minimum number of packets lost on remote side. | [optional] 
**remote_normdevrxploss** | **double** | Average number of packets lost on remote side. | [optional] 
**remote_stdevrxploss** | **double** | Standard deviation packets lost on remote side. | [optional] 
**local_maxrxploss** | **double** | Maximum number of packets lost on local side. | [optional] 
**local_minrxploss** | **double** | Minimum number of packets lost on local side. | [optional] 
**local_normdevrxploss** | **double** | Average number of packets lost on local side. | [optional] 
**local_stdevrxploss** | **double** | Standard deviation packets lost on local side. | [optional] 
**rtt** | **double** | Total round trip time. | [optional] 
**maxrtt** | **double** | Maximum round trip time. | [optional] 
**minrtt** | **double** | Minimum round trip time. | [optional] 
**normdevrtt** | **double** | Average round trip time. | [optional] 
**stdevrtt** | **double** | Standard deviation round trip time. | [optional] 
**local_ssrc** | [**\Swagger\Client\Model\Int**](Int.md) | Our SSRC. | [optional] 
**remote_ssrc** | [**\Swagger\Client\Model\Int**](Int.md) | Their SSRC. | [optional] 
**txoctetcount** | [**\Swagger\Client\Model\Int**](Int.md) | Number of octets transmitted. | [optional] 
**rxoctetcount** | [**\Swagger\Client\Model\Int**](Int.md) | Number of octets received. | [optional] 
**channel_uniqueid** | **string** | The Asterisk channel&#39;s unique ID that owns this instance. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


