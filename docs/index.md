# API Developer Guide

## Get Affiliate UIDs
  - **Method**: ***GET***
  - **Url**: user-api-path/b2b/agent/affiliate_uids?uid=1234567&startTime=1234567890123&endTime=1234567890123&page=1&pageSize=100
  
### Request Params
    
|  Parameter  |     Type    |  Mandatory  | Description |   Example   |
|-------------|-------------|-------------|-------------|-------------|
|  uid   |  Long  |  No    | KOL uid     |  1234567    |
|  startTime  |  Long  |  No    | Start timestamp in UTC     |  1738734183391    |
|  endTime    |  Long  |  No    | End timestamp in UTC     |  1738734183391    |
|  page    |  int  |  No    | Paging for pages, starting from page 1, Default 1     |  1    |
|  pageSize    |  int  |  No    | Paging size, default is 10     |  10    |

### Response 

|  Parameter  |     Type     | Description |
|-------------|--------------|--------------|
|  uid   |  string      |   KOL uid    |
|  registerTime  |  Long  |  Registration timestamp, unit: milliseconds    |
|  kycResult    |  boolean  |  KYC status    |

### Example Response

```json
{
  "code": 200,
  "data": [
    {
      "uid": "1098631518919999489",
      "kycResult": false,
      "registerTime": 1739863765000
    }
  ],
  "success": "success"
}
```

## Get Affiliate Commission
  - **Method**: ***GET***
  - **Url**: user-api-path/b2b/agent/affiliate_commission?uid=1234567&startTime=1234567890123&endTime=1234567890123&coin=USDT&productType=FUTURES&page=1&pageSize=100
  
### Request Params
    
|  Parameter  |     Type    |  Mandatory  | Description |   Example   |
|-------------|-------------|-------------|-------------|-------------|
|  uid   |  Long  |  No    | KOL uid     |  1234567    |
|  startTime  |  Long  |  No    | Start timestamp in UTC     |  1738734183391    |
|  endTime    |  Long  |  No    | End timestamp in UTC     |  1738734183391    |
| coin |  string  |  No  |  USDT or BTC... |  USDT  |
|  productType  |  string  |  No  |  SPOT or SWAP...  |  SWAP  |
|  page    |  int  |  No    | Paging for pages, starting from page 1, Default 1     |  1    |
|  pageSize    |  int  |  No    | Paging size, default is 10     |  10    |

### Response 

|  Parameter  |     Type     | Description |
|-------------|--------------|--------------|
|  uid   |  string      |   KOL uid    |
|  date  |  Long  |  Registration timestamp, unit: milliseconds    |
|  coin    |  string  |  USDT or BTC...  |
|  productType  | string  |  SPOT or SWAP...  |
|  fee  |  string  |  Net Trading Fee  |
|  commission  |  string  |  Paid Commission  |

### Example Response

```json
{
    "code":200,
    "data":[
        {
            "coin":"USDT",
            "commission":0.2937887,
            "date":"1580460059000",
            "fee":0.01,
            "productType":"SWAP",
            "uid":"430043912850112512"
        }
    ],
    "success":"success"
}
```

