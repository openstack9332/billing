getContractDemandCostList
======================================

<h3>개요</h3>
계약 청구 비용 리스트를 조회합니다.

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
   <td>demandTypeCode</td>
   <td>No</td>
   <td>String</td>
   <td></td>
   <td>청구 유형 코드</td>
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

요청 API : /billing/v1/cost/getContractDemandCostList?startMonth=202201&endMonth=202202&demandTypeCode=BST&responseFormatType=json

**핵심 정보**

```
{"getContractDemandCostListResponse": {
  "requestId": "8b0d5f45-54fb-49b7-910a-a9c1927c106e",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 52,
  "contractDemandCostList": [
    {
      "loginId": "klaytn@hongikit.com",
      "regionCode": "KR",
      "demandType": {
        "code": "BST",
        "codeName": "Block Storage"
      },
      "demandTypeDetail": {
        "code": "BST",
        "codeName": "Block Storage Usage"
      },
      "contract": {
        "loginId": "klaytn@hongikit.com",
        "contractNo": "7991988",
        "conjunctionContractNo": "",
        "contractType": {
          "code": "BST",
          "codeName": "Block Storage"
        },
        "contractStatus": {
          "code": "NLEND",
          "codeName": "Normal termination"
        },
        "contractStartDate": "2021-12-01T10:16:39+0900",
        "contractEndDate": "2022-01-04T17:22:41+0900",
        "instanceName": "klaytn-en1",
        "regionCode": "KR",
        "platformType": {
          "code": "VPC",
          "codeName": "VPC"
        },
        "contractProductList": [
          {
            "contractProductSequence": "1",
            "beforeContractProductSequence": "",
            "productCode": "SPBSTBSTAD000006",
            "priceNo": "323",
            "instanceNo": "9151438",
            "productItemKind": {
              "code": "BST",
              "codeName": "Block storage"
            },
            "productRatingType": {
              "code": "BST",
              "codeName": "Block Storage Usage"
            },
            "serviceStatus": {
              "code": "END",
              "codeName": "Termination"
            },
            "serviceStartDate": "2021-12-01T10:16:39+0900",
            "serviceEndDate": "2022-01-04T17:22:41+0900",
            "productSize": 1073741824000,
            "productCount": 0,
            "productSizeType": {
              "code": "GEN",
              "codeName": "General"
            },
            "usageList": []
          }
        ]
      },
      "demandMonth": "202201",
      "unitUsageQuantity": 90,
      "packageUnitUsageQuantity": 0,
      "totalUnitUsageQuantity": 90,
      "usageUnit": {
        "code": "USAGE_TIME",
        "codeName": "Usage time(Prorated)"
      },
      "productPrice": 0.16,
      "useAmount": 14400,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "defaultAmount": 0,
      "promiseDiscountAmount": 0,
      "demandAmount": 0,
      "writeDate": "2022-02-01T08:28:04+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "regionCode": "KR",
      "demandType": {
        "code": "BST",
        "codeName": "Block Storage"
      },
      "demandTypeDetail": {
        "code": "BST",
        "codeName": "Block Storage Usage"
      },
      "contract": {
        "loginId": "klaytn@hongikit.com",
        "contractNo": "7991991",
        "conjunctionContractNo": "",
        "contractType": {
          "code": "BST",
          "codeName": "Block Storage"
        },
        "contractStatus": {
          "code": "NLEND",
          "codeName": "Normal termination"
        },
        "contractStartDate": "2021-12-01T10:16:58+0900",
        "contractEndDate": "2022-01-04T17:22:41+0900",
        "instanceName": "klaytn-en2",
        "regionCode": "KR",
        "platformType": {
          "code": "VPC",
          "codeName": "VPC"
        },
        "contractProductList": [
          {
            "contractProductSequence": "1",
            "beforeContractProductSequence": "",
            "productCode": "SPBSTBSTAD000006",
            "priceNo": "323",
            "instanceNo": "9151441",
            "productItemKind": {
              "code": "BST",
              "codeName": "Block storage"
            },
            "productRatingType": {
              "code": "BST",
              "codeName": "Block Storage Usage"
            },
            "serviceStatus": {
              "code": "END",
              "codeName": "Termination"
            },
            "serviceStartDate": "2021-12-01T10:16:58+0900",
            "serviceEndDate": "2022-01-04T17:22:41+0900",
            "productSize": 1073741824000,
            "productCount": 0,
            "productSizeType": {
              "code": "GEN",
              "codeName": "General"
            },
            "usageList": []
          }
        ]
      },
      "demandMonth": "202201",
      "unitUsageQuantity": 90,
      "packageUnitUsageQuantity": 0,
      "totalUnitUsageQuantity": 90,
      "usageUnit": {
        "code": "USAGE_TIME",
        "codeName": "Usage time(Prorated)"
      },
      "productPrice": 0.16,
      "useAmount": 14400,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "defaultAmount": 0,
      "promiseDiscountAmount": 0,
      "demandAmount": 0,
      "writeDate": "2022-02-01T08:28:04+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    ...
```




