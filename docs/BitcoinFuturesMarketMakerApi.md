# quant_trading.BitcoinFuturesMarketMakerApi

All URIs are relative to *https://www.quant-trading.network/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_algo_params**](BitcoinFuturesMarketMakerApi.md#get_algo_params) | **GET** /bitcoinFuturesMm/algo-params | 
[**post_exec_algo**](BitcoinFuturesMarketMakerApi.md#post_exec_algo) | **POST** /bitcoinFuturesMm/exec-algo | 

# **get_algo_params**
> AlgoParamsResponse get_algo_params()



Get algorithm parameters

### Example
```python
from __future__ import print_function
import time
import quant_trading
from quant_trading.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = quant_trading.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'

# create an instance of the API class
api_instance = quant_trading.BitcoinFuturesMarketMakerApi(quant_trading.ApiClient(configuration))

try:
    api_response = api_instance.get_algo_params()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BitcoinFuturesMarketMakerApi->get_algo_params: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AlgoParamsResponse**](AlgoParamsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_exec_algo**
> ExecAlgoResponse post_exec_algo(body)



Determine algorithm execution

### Example
```python
from __future__ import print_function
import time
import quant_trading
from quant_trading.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = quant_trading.Configuration()
configuration.api_key['X-API-KEY'] = 'YOUR_API_KEY'

# create an instance of the API class
api_instance = quant_trading.BitcoinFuturesMarketMakerApi(quant_trading.ApiClient(configuration))
body = quant_trading.ExecPositionManagerAlgoRequest(quant_trading.StakeState.CLOSED, quant_trading.StakeState.CLOSED, 0.0, 0.0, 0.0, 0.0, 0.0) # ExecPositionManagerAlgoRequest | A JSON object containing the current position manager algorithm information.

try:
    api_response = api_instance.post_exec_algo(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BitcoinFuturesMarketMakerApi->post_exec_algo: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ExecPositionManagerAlgoRequest**](ExecPositionManagerAlgoRequest.md)| A JSON object containing the current position manager algorithm information. | 

### Return type

[**ExecAlgoResponse**](ExecAlgoResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

