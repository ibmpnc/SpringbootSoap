# SpringbootSoap
Soap Service, Soap Client applications has been created

Server :
Input Request :
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:loan="http://www.springboot.com/spring/soap/api/loanEligibility">
   <soapenv:Header/>
   <soapenv:Body>
      <loan:CustomerRequest>
         <loan:customerName>Sriram</loan:customerName>
         <loan:age>31</loan:age>
         <loan:yearlyIncome>5000000</loan:yearlyIncome>
         <loan:cibilScore>700</loan:cibilScore>
         <loan:employmentMode>Software</loan:employmentMode>
      </loan:CustomerRequest>
   </soapenv:Body>
</soapenv:Envelope>

Output Response :
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Header/>
   <SOAP-ENV:Body>
      <ns2:Acknowledgement xmlns:ns2="http://www.springboot.com/spring/soap/api/loanEligibility">
         <ns2:isEligible>true</ns2:isEligible>
         <ns2:approvedAmount>500000</ns2:approvedAmount>
      </ns2:Acknowledgement>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

Criterias :
 1.Person age should in between 30 to 60
 2.CriteriaMismatch>minimum income should be more than 200000
 3.CriteriaMismatch>Low CIBIL Score please try after 6 month


Client:

Client will talk to Springboot Soap server based on the above condition it will get the response.
url POST : http://localhost:9090/getLoanStatus

Input:(JSON)
{
	"customerName":"Abc",
    "age":40,
    "yearlyIncome":500000,
    "cibilScore":700,
    "employmentMode":"Gov"
}

Output:(JSON)
{
    "isEligible": true,
    "approvedAmount": 500000,
    "criteriaMismatch": []
}

Kindly, please let me know if you have any doubts or any concerns.
