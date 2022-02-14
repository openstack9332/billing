getCostRelationCodeList
==================

<h3>개요</h3>
비용연관코드 리스트를 조회합니다.

비용연관코드는 다른 사용량/비용 조회 API에서 사용할 수 있습니다.

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
  <td>contractTypeCode</td>
  <td>No</td>
  <td>String</td>
  <td></td>
  <td>계약구분코드</td>
 </tr>
 <tr>
  <td>productItemKindCode</td>
  <td>No</td>
  <td>String</td>
  <td></td>
  <td>상품품목종류코드</td>
 </tr>
 <tr>
  <td>productRatingTypeCode</td>
  <td>No</td>
  <td>String</td>
  <td></td>
  <td>상품과금유형코드</td>
 </tr>
 <tr>
  <td>meteringTypeCode</td>
  <td>No</td>
  <td>String</td>
  <td></td>
  <td>미터링구분코드</td>
 </tr>
 <tr>
  <td>responseFormatType</td>
  <td>No</td>
  <td>String</td>
  <td></td>
  <td>응답 결과의 포맷 타입<br data-tomark-pass="">Options : xml | json<br data-tomark-pass="">Default : xml</td>
 </tr>
 </tbody>
</table>


## Response

요청 API : /billing/v1/cost/getCostRelationCodeList?contractTypeCode=VSVR&productItemKindCode=VSVR&responseFormatType=json

응답 결과 : VSVR(VPC)에 대한 비용연관코드 리스트 조회

**핵심 정보**

```
 {"getCostRelationCodeListResponse": {
  "requestId": "604e18b0-9e14-4320-9863-e2811a6617d0",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 2,
  "costRelationCodeList": [
    {
      "contractType": {
        "code": "VSVR",
        "codeName": "Server(VPC)"
      },
      "productItemKind": {
        "code": "VSVR",
        "codeName": "Server (VPC)"
      },
      "productRatingType": {
        "code": "VSVR",
        "codeName": "Server (VPC) Usage"
      },
      "meteringType": {
        "code": "VSVR",
        "codeName": "Server (VPC) Usage"
      },
      "demandType": {
        "code": "VSVR",
        "codeName": "Server (VPC)"
      },
      "demandTypeDetail": {
        "code": "VSVR",
        "codeName": "Server (VPC) Usage"
      },
      "productDemandType": {
        "code": "VSVR",
        "codeName": "Server(VPC)"
      }
    },
    {
      "contractType": {
        "code": "VSVR",
        "codeName": "Server(VPC)"
      },
      "productItemKind": {
        "code": "VSVR",
        "codeName": "Server (VPC)"
      },
      "productRatingType": {
        "code": "VSVR",
        "codeName": "Server (VPC) Usage"
      },
      "meteringType": {
        "code": "VSVRT",
        "codeName": "Server (VPC) Stop Usage"
      },
      "demandType": {
        "code": "VSVR",
        "codeName": "Server (VPC)"
      },
      "demandTypeDetail": {
        "code": "VSVRT",
        "codeName": "Server (VPC) Stop Usage"
      },
      "productDemandType": {
        "code": "VSVR",
        "codeName": "Server(VPC)"
      }
    }
  ]
}}
```









