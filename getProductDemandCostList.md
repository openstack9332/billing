getProductDemandCostList
==================

<h3>개요</h3>
상품 청구 비용 리스트를 조회

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
   <td>productDemandTypeCode</td>
   <td>No</td>
   <td>String</td>
   <td></td>
   <td>상품청구유형코드</td>
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

<h3>Ex)</h3>

API : /billing/v1/cost/getProductDemandCostList?startMonth=202201&endMonth=202202

2022년01월 ~ 2022년02월 조회

<h3>Ex)</h3>

API : /billing/v1/cost/getProductDemandCostList?productDemandTypeCode=BST

Block Storage에 대한 상품 청구 비용 리스트 조회

<h3>Ex)</h3>

API : /billing/v1/cost/getProductDemandCostList?responseFormatType=json

포맷 타입 Json

## Response

요청 API : /billing/v1/cost/getProductDemandCostList?startMonth=202201&endMonth=202201&responseFormatType=json

**핵심 정보**

<table border="1" width="100%">
 <thead>
  <tr>
   <th>서비스</th>
   <th>이용 요금</th>
  </tr>
 </thead>
 <tbody>   
  <tr>
    <td>Block Storage</td>
    <td>987590</td>
  </tr>
  <tr>
    <td>Cloud Insight</td>
    <td>0</td>
  </tr> 
  <tr>
    <td>Network Traffic Monitoring</td>
    <td>0</td>
  </tr>  
  <tr>
    <td>Network - Server&amp;LoadBalancer</td>
    <td>114670</td>
  </tr>  
  <tr>
    <td>Public IP</td>
    <td>9150</td>
  </tr>
  <tr>
    <td>Software</td>
    <td>0</td>
  </tr>
  <tr>
    <td>Load Balancer (VPC)</td>
    <td>19340</td>
  </tr>
  <tr>
     <td>Server(VPC)</td>
     <td>749780</td>
  </tr> 
 </tbody>
</table>

<table border="1" width="100%">
 <thead>
  <tr>
   <th>속성</th>
   <th>설명</th>
  </tr>
 </thead>
 <tbody>   
  <tr>
    <td>promiseDiscountAmount </td>
    <td>약정 할인</td>
  </tr>
  <tr>
    <td>promotionDiscountAmount</td>
    <td></td>
  </tr> 
  <tr>
    <td>etcDiscountAmount</td>
    <td>기타 할인</td>
  </tr>  
  <tr>
    <td>productDiscountAmount</td>
    <td></td>
  </tr>  
  <tr>
    <td>creditDiscountAmount</td>
    <td>크레딧 할인</td>
  </tr>
  <tr>
    <td>defaultAmount</td>
    <td></td>
  </tr>
  <tr>
    <td>useAmount</td>
    <td>사용 요금</td>
  </tr>
  <tr>
     <td>demandAmount</td>
     <td></td>
  </tr>
  <tr>
     <td>writeDate</td>
     <td>사용 날짜</td>
  </tr> 
  <tr>
     <td>memberPriceDiscountAmount</td>
     <td>회원요금제 할인</td>
  </tr> 
  <tr>
     <td>memberPromiseDiscountAddAmount</td>
     <td>회원약정요금제 할인</td>
  </tr> 
 </tbody>
</table>

<pre>
{"getProductDemandCostListResponse": {
  "requestId": "9d9c5923-c7c2-438b-a5b1-42cfd55c5192",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 8,
  "productDemandCostList": [
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "BST",
        "codeName": "Block Storage"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 987590,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
</pre>

## Response ( ALL )

<pre>
{"getProductDemandCostListResponse": {
  "requestId": "9d9c5923-c7c2-438b-a5b1-42cfd55c5192",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 8,
  "productDemandCostList": [
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "BST",
        "codeName": "Block Storage"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 987590,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "CLWAT",
        "codeName": "Cloud Insight"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 0,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "NETMN",
        "codeName": "Network Traffic Monitoring"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 0,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "NET_SVR",
        "codeName": "Network - Server&LoadBalancer"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 114670,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "PBLIP",
        "codeName": "Public IP"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 9150,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "SW",
        "codeName": "Software"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 0,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "VLB",
        "codeName": "Load Balancer (VPC)"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 19340,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "productDemandType": {
        "code": "VSVR",
        "codeName": "Server(VPC)"
      },
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "defaultAmount": 0,
      "useAmount": 749780,
      "demandAmount": 0,
      "writeDate": "2022-02-01T17:57:18+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    }
  ]
}}
</pre>

