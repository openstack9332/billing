# getDemandCostList

<h3>개요</h3>

청구 비용 리스트를 조회합니다.

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
<td>responseFormatType</td>
<td>No</td>
<td>String</td>
<td></td>
<td>- 응답 결과의 포맷 타입<br data-tomark-pass="">- Options: xml | json<br data-tomark-pass="">- Default: xml</td>
</tr>
</tbody>
</table>

## Response

요청 API : /billing/v1/cost/getDemandCostList?startMonth=202201&endMonth=202202&responseFormatType=json

응답 결과 : 2022년 01월 ~ 2022년 02월에 대한 요금 리스트 조회

```
 {"getDemandCostListResponse": {
  "requestId": "523259c7-1a3d-42c2-9c3e-179e851b00fe",
  "returnCode": "0",
  "returnMessage": "success",
  "totalRows": 2,
  "demandCostList": [
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202201",
      "demandNo": "4126895",
      "integrationDemandNo": "",
      "demandAttribute": {
        "code": "GEN",
        "codeName": "General"
      },
      "useAmount": 1880530,
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "customerDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "under100DiscountAmount": 0,
      "under1000DiscountAmount": 0,
      "coinUseAmount": 0,
      "defaultAmount": 0,
      "thisMonthDemandAmount": 0,
      "thisMonthVatRatio": 0.1,
      "thisMonthVatAmount": 0,
      "thisMonthAmountIncludingVat": 0,
      "totalDemandAmount": 0,
      "isPaidUp": true,
      "paidUpDate": "2022-02-01T17:59:22+0900",
      "overduePlusAmount": 0,
      "overdueRatio": 0.0,
      "thisMonthOverdueAmount": 0,
      "beforeMonthDemandNo": "3936015",
      "totalOverdueAmount": 0,
      "writeDate": "2022-02-01T17:59:13+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    },
    {
      "loginId": "klaytn@hongikit.com",
      "demandMonth": "202202",
      "demandNo": "4307765",
      "integrationDemandNo": "",
      "demandAttribute": {
        "code": "GEN",
        "codeName": "General"
      },
      "useAmount": 1357040,
      "promiseDiscountAmount": 0,
      "promotionDiscountAmount": 0,
      "etcDiscountAmount": 0,
      "customerDiscountAmount": 0,
      "productDiscountAmount": 0,
      "creditDiscountAmount": 0,
      "under100DiscountAmount": 0,
      "under1000DiscountAmount": 0,
      "coinUseAmount": 0,
      "defaultAmount": 0,
      "thisMonthDemandAmount": 0,
      "thisMonthVatRatio": 0.1,
      "thisMonthVatAmount": 0,
      "thisMonthAmountIncludingVat": 0,
      "totalDemandAmount": 0,
      "isPaidUp": true,
      "paidUpDate": "2022-02-14T10:07:30+0900",
      "overduePlusAmount": 0,
      "overdueRatio": 0.0,
      "thisMonthOverdueAmount": 0,
      "beforeMonthDemandNo": "4126895",
      "totalOverdueAmount": 0,
      "writeDate": "2022-02-14T09:26:53+0900",
      "memberPriceDiscountAmount": 0,
      "memberPromiseDiscountAddAmount": 0
    }
  ]
}}
```
