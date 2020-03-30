# ExecAlgoResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**decision** | **str** | The decision taken by the algorithm. Whether to open a long/short position or to cancel the previous attempt. | [optional] 
**decision_timestamp** | **datetime** | The timestamp this decision was taken by the algorithm. | [optional] 
**next_decision_timestamp** | **datetime** | The timestamp when the user will be able to get a new decision from the algorithm. | [optional] 
**milliseconds_to_next_decision** | **int** | The milliseconds left for the new decision when user will be able to get a new decision from the algorithm. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

