# Get Affiliate UIDs
  - Method: GET
  - Url: user-api-path/b2b/agent/affiliate_uids?uid=1234567&startTime=1234567890123&endTime=1234567890123&page=1&pageSize=100
  
### Request Params
    
|  Parameter  |     Type    |  Mandatory  | Description |   Example   |
|-------------|-------------|-------------|-------------|-------------|
|  uid        |  Long       |  No         | KOL uid     |  1234567    |
|  startTime  |  Long       |  No         | Start timestamp in UTC     |  1738734183391    |
|  endTime    |  Long       |  No         | End timestamp in UTC     |  1738734183391    |
|  page    |  int       |  No         | Paging for pages, starting from page 1, Default 1     |  1    |
|  pageSize    |  int       |  No         | Paging size, default is 10     |  10    |

### Response 

|  Parameter  |     Type     | Description |
|-------------|--------------|--------------|
|  uid        |  String      |   KOL uid    |
|  registerTime  |  Long       |  Registration timestamp, unit: milliseconds         |
|  kycResult    |  boolean       |  KYC status         |

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
