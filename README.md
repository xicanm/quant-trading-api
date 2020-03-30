# quant-trading-api
This API will use JSON.         JSON looks like this:                {         \"key\": \"value\",         \"anotherKey\": \"anotherValue\"       }

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.python.PythonClientCodegen
For more information, please visit [https://www.quant-trading.network/support/](https://www.quant-trading.network/support/)

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install quant-trading-api
```
(you may need to run `pip` with root permission: `sudo pip install `)

Then import the package:
```python
import quant_trading 
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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
api_instance = quant_trading.BitcoinFuturesManagerApi(quant_trading.ApiClient(configuration))

try:
    api_response = api_instance.get_algo_params()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BitcoinFuturesManagerApi->get_algo_params: %s\n" % e)

body = quant_trading.ExecPositionManagerAlgoRequest(quant_trading.StakeState.CLOSED, quant_trading.StakeState.CLOSED, 0.0, 0.0, 0.0, 0.0, 0.0) # ExecPositionManagerAlgoRequest | A JSON object containing the current position manager algorithm information.

try:
    api_response = api_instance.post_exec_algo(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BitcoinFuturesManagerApi->post_exec_algo: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://www.quant-trading.network/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BitcoinFuturesManagerApi* | [**get_algo_params**](docs/BitcoinFuturesManagerApi.md#get_algo_params) | **GET** /bitcoinFuturesManager/algo-params | 
*BitcoinFuturesManagerApi* | [**post_exec_algo**](docs/BitcoinFuturesManagerApi.md#post_exec_algo) | **POST** /bitcoinFuturesManager/exec-algo | 
*BitcoinFuturesMarketMakerApi* | [**get_algo_params**](docs/BitcoinFuturesMarketMakerApi.md#get_algo_params) | **GET** /bitcoinFuturesMm/algo-params | 
*BitcoinFuturesMarketMakerApi* | [**post_exec_algo**](docs/BitcoinFuturesMarketMakerApi.md#post_exec_algo) | **POST** /bitcoinFuturesMm/exec-algo | 
*BitcoinFuturesSwingerApi* | [**get_algo_params**](docs/BitcoinFuturesSwingerApi.md#get_algo_params) | **GET** /bitcoinFuturesSwinger/algo-params | 
*BitcoinFuturesSwingerApi* | [**post_exec_algo**](docs/BitcoinFuturesSwingerApi.md#post_exec_algo) | **POST** /bitcoinFuturesSwinger/exec-algo | 

## Documentation For Models

 - [AlgoParamsResponse](docs/AlgoParamsResponse.md)
 - [AvgOpenPositionHours](docs/AvgOpenPositionHours.md)
 - [ClosedPositionHours](docs/ClosedPositionHours.md)
 - [CurrentPositionPct](docs/CurrentPositionPct.md)
 - [CurrentUnrealisedPct](docs/CurrentUnrealisedPct.md)
 - [Error](docs/Error.md)
 - [ExecAlgoResponse](docs/ExecAlgoResponse.md)
 - [ExecPositionManagerAlgoRequest](docs/ExecPositionManagerAlgoRequest.md)
 - [ExecPositionSwingerAlgoRequest](docs/ExecPositionSwingerAlgoRequest.md)
 - [LastOpenStakeHours](docs/LastOpenStakeHours.md)
 - [OpenPositionHours](docs/OpenPositionHours.md)
 - [PositionState](docs/PositionState.md)
 - [StakeState](docs/StakeState.md)
 - [XRateLimitLimit](docs/XRateLimitLimit.md)
 - [XRateLimitRemaining](docs/XRateLimitRemaining.md)
 - [XRateLimitReset](docs/XRateLimitReset.md)

## Documentation For Authorization


## ApiKeyAuth

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header


## Author

support@quant-trading.network
