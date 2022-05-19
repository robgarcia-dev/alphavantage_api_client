# alphavantage-api-client
Build a simple client to talk to Alphavantage API

## You have three ways to define your api key:
1. in an ini file in [your profile root]/.alphavantage
```
[access]
api_key=[example api key here]
```
3. Pass to client builder
```
client = AlphavantageClient().with_api_key('[you key here]')
```
5. Pass in as parameter
```
event = {
 "api_key":"[you key here]",
 "symbol":"TSLA"
 }
result = client.get_stock_price(event)
```

## Sample Usage Specifying Api Key in Client Builder
```
event = {
        "symbol":"TSLA"
    }
    result = {}
    client = AlphavantageClient().with_api_key('[you key here]')
    result['overview'] = client.get_company_overview(event)
    result['latest_stock_price'] = client.get_latest_stock_price(event)
    result['stock_price'] = client.get_stock_price(event)
    result['earnings'] = client.get_earnings(event)
    result['latest_earnings'] = client.get_latest_earnings(event)
    result['cash_flow'] = client.get_cash_flow(event)
    result['latest_cash_flow'] = client.get_latest_cash_flow(event)
    result['income_statement'] = client.get_income_statement_for_symbol(event)
    result['latest_income_statement'] = client.get_latest_income_statement_for_symbol(event)
    print(json.dumps(result))
```

## Sample Usage Specifying Api Key in request event
```
event = {
        "symbol":"TSLA",
        "api_key":"[your api key here]"
    }
    result = {}
    client = AlphavantageClient()
    result['overview'] = client.get_company_overview(event)
    result['latest_stock_price'] = client.get_latest_stock_price(event)
    result['stock_price'] = client.get_stock_price(event)
    result['earnings'] = client.get_earnings(event)
    result['latest_earnings'] = client.get_latest_earnings(event)
    result['cash_flow'] = client.get_cash_flow(event)
    result['latest_cash_flow'] = client.get_latest_cash_flow(event)
    result['income_statement'] = client.get_income_statement_for_symbol(event)
    result['latest_income_statement'] = client.get_latest_income_statement_for_symbol(event)
    print(json.dumps(result))
```

## Sample Usage Specifying Api Key in ini file
### On mac/linux based machines run the following command BUT use your own API KEY
```
echo -e "[access]\napi_key=[your key here]" > ~/.alphavantage
```

### Now try the below
```
event = {
        "symbol":"TSLA"
    }
    result = {}
    client = AlphavantageClient()
    result['overview'] = client.get_company_overview(event)
    result['latest_stock_price'] = client.get_latest_stock_price(event)
    result['stock_price'] = client.get_stock_price(event)
    result['earnings'] = client.get_earnings(event)
    result['latest_earnings'] = client.get_latest_earnings(event)
    result['cash_flow'] = client.get_cash_flow(event)
    result['latest_cash_flow'] = client.get_latest_cash_flow(event)
    result['income_statement'] = client.get_income_statement_for_symbol(event)
    result['latest_income_statement'] = client.get_latest_income_statement_for_symbol(event)
    print(json.dumps(result))
```



