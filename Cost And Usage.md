Cost And Usage 
=========

<h3>개요</h3>

네이버 클라우드 플랫폼에서 사용한 계약의 사용량 / 이용금액을 조회하는 API입니다. Billing API 는 RESTful 형태로 제공됩니다. HTTP 방식의 GET/POST 메서드 호출을 통해서 이루어집니다.

<h3>공통 설정</h3>

<br>

**공통 API** 

<div class="code-toolbar"><pre class="  language-http"><code data-language="http" class="  language-http">GET or POST
<span class="token header-name keyword">https:</span>//billingapi.apigw.ntruss.com
</code></pre><div class="toolbar">

## 요청 헤더

<table>
 <thead>
  <tr>
   <th>헤더명</th>
   <th>설명</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>x-ncp-apigw-timestamp</td>
   <td>1970 년 1 월 1 일 00:00:00 협정 세계시(UTC)부터의 경과 시간을 밀리초(Millisecond)로 나타낸 것이다.<br data-tomark-pass="">API Gateway 서버와 시간 차가 5 분 이상 나는 경우 유효하지        않은 요청으로 간주</td>
  </tr>
  <tr>
   <td>x-ncp-iam-access-key</td>
   <td>네이버 클라우드 플랫폼에서 발급받은 API Key 또는 IAM에서 발급받은 AccessKey</td>
  </tr>
  <tr>
   <td>x-ncp-apigw-signature-v2</td>
   <td>위 예제의 Body를 AccessKey와 맵핑되는 SecretKey로 암호화한 서명<br data-tomark-pass="">HMAC 암호화 알고리즘은 HmacSHA256 사용</td>
  </tr>
  </tbody>
</table>

<br>
 
## 오퍼레이션

API :
[/billing/v1/cost/getProductDemandCostList](https://github.com/openstack9332/billing/blob/main/getProductDemandCostList.md)

상품 청구 비용 리스트 조회

 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 


 
 

