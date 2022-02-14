getContractUsageList
==================

<h3>개요</h3>
계약 사용량 리스트를 조회합니다.

<h3>요청 파라미터</h3>

<table>
 <thead>
  <tr>
   <th>파라미터명</th>
   <th>필수 여부</th>
   <th>타입</th>
   <th>제약 사항</th>
   <th>설명</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>startMonth</td>
   <td>Yes</td>
   <td>String</td>
   <td>최대 3개월 동시 조회 가능</td>
   <td>조회 시작 월 (yyyyMM)<br data-tomark-pass=""> &lt;예시&gt; 202001</td>
  </tr>
  <tr>
   <td>endMonth</td>
   <td>Yes</td>
   <td>String</td>
   <td>최대 3개월 동시 조회 가능</td>
   <td>조회 마지막 월 (yyyyMM)<br data-tomark-pass=""> &lt;예시&gt; 202001</td>
  </tr>
  <tr>
   <td>contractTypeCode</td>
   <td>No</td>
   <td>String</td>
   <td></td>
   <td>계약유형코드</td>
  </tr>
  <tr>
   <td>responseFormatType</td>
   <td>No</td>
   <td>String</td>
   <td></td>
   <td>- 응답 결과의 포맷 타입<br data-tomark-pass="">- Options: xml | json<br data-tomark-pass="">- Default: xml</td>
  </tr>
 </tbody>
</table>

## Response

요청 API : /billing/v1/cost/getContractUsageList?startMonth=202201&endMonth=202202&contractTypeCode=NATGW&responseFormatType=json

응답 결과 : 2022년 01월 ~ 2022년 02월 NAT Gateway에 대한 요금 조회

**핵심 정보**

```
 {"getContractUsageListResponse": {
  "requestId": "c69bc9f3-d5d2-4934-a83b-f2054174154f",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 1,
  "contractList": [
    {
      "loginId": "klaytn@hongikit.com",
      "contractNo": "8705294",
      "conjunctionContractNo": "",
      "contractType": {
        "code": "NATGW",
        "codeName": "NAT Gateway"
      },
      "contractStatus": {
        "code": "NLEND",
        "codeName": "Normal termination"
      },
      "contractStartDate": "2022-02-07T18:11:01+0900",
      "contractEndDate": "2022-02-08T14:07:16+0900",
      "instanceName": "fg-klaytn-nat-gw",
      "regionCode": "KR",
      "platformType": {
        "code": "VPC",
        "codeName": "VPC"
      },
      "contractProductList": [
        {
          "contractProductSequence": "2",
          "beforeContractProductSequence": "",
          "productCode": "SPNATGW000000001",
          "priceNo": "3081",
          "instanceNo": "10061915",
          "productItemKind": {
            "code": "NATGW",
            "codeName": "NAT Gateway"
          },
          "productRatingType": {
            "code": "NATNW",
            "codeName": "NAT Gateway Data Throughput"
          },
          "serviceStatus": {
            "code": "END",
            "codeName": "Termination"
          },
          "serviceStartDate": "2022-02-07T18:11:01+0900",
          "serviceEndDate": "2022-02-08T14:07:16+0900",
          "productSize": 0,
          "productCount": 0,
          "productSizeType": {},
          "usageList": [
            {
              "meteringType": {},
              "useMonth": "",
              "usageQuantity": 0,
              "unit": {
                "code": "USAGE_1BYTE",
                "codeName": "Usage (1 Byte)"
              }
            }
          ]
        },
        {
          "contractProductSequence": "1",
          "beforeContractProductSequence": "",
          "productCode": "SPNATGW000000001",
          "priceNo": "3080",
          "instanceNo": "10061915",
          "productItemKind": {
            "code": "NATGW",
            "codeName": "NAT Gateway"
          },
          "productRatingType": {
            "code": "NATMN",
            "codeName": "NAT Gateway Maintenence"
          },
          "serviceStatus": {
            "code": "END",
            "codeName": "Termination"
          },
          "serviceStartDate": "2022-02-07T18:11:01+0900",
          "serviceEndDate": "2022-02-08T14:07:16+0900",
          "productSize": 0,
          "productCount": 0,
          "productSizeType": {},
          "usageList": [
            {
              "meteringType": {
                "code": "NATMN",
                "codeName": "NAT Gateway Maintenence"
              },
              "useMonth": "202202",
              "usageQuantity": 71775,
              "unit": {
                "code": "USAGE_SEC",
                "codeName": "Usage time (per second)"
              }
            }
          ]
        }
      ]
    }
  ]
}}
```
