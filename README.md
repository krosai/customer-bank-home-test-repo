# customer-bank-home-test-repo

**mule server version-4.3.0
Anypoint studio version-7.6.0**
**Control plane-Mule controlled**  
**Runtime plane- Client controlled on premise deployment**

Features of the API

1. Enabled HTTPS
2. Have root CA signed keystore and truststore
3. Have JWT validation using Anth0 using grand type as **Client_Credentials** on get flow
4. Have JWT validation using Anth0 using grand type as **Authorization_code** on post flow
5. Implenment validation check to check the integrity of the payload
6. Implement Munit test for all the flows
7. Externalize the properties
8. Implement secure property configuraiton to encrypt sensitive data
9. Implement domain project


Get flow
case 1: 
Request - https://localhost:8124/hello?Foo=Bar 
Authorization code - eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6ImdlUldnekZYUERBVnhqTzlNZzROZSJ9.eyJpc3MiOiJodHRwczovL2Rldi1yOTJ1NnJzNC51cy5hdXRoMC5jb20vIiwic3ViIjoiYTNMY2tvUk5lQzFDcE4zUk56Z1p4U1V2eHlFTmM4WkNAY2xpZW50cyIsImF1ZCI6Imh0dHBzOi8vZGV2LXI5MnU2cnM0LnVzLmF1dGgwLmNvbS9hcGkvdjIvIiwiaWF0IjoxNjE0MTI1ODU5LCJleHAiOjE2MTQyMTIyNTksImF6cCI6ImEzTGNrb1JOZUMxQ3BOM1JOemdaeFNVdnh5RU5jOFpDIiwic2NvcGUiOiJyZWFkOmNsaWVudF9ncmFudHMgY3JlYXRlOmNsaWVudF9ncmFudHMgZGVsZXRlOmNsaWVudF9ncmFudHMgdXBkYXRlOmNsaWVudF9ncmFudHMgcmVhZDp1c2VycyB1cGRhdGU6dXNlcnMgZGVsZXRlOnVzZXJzIGNyZWF0ZTp1c2VycyByZWFkOnVzZXJzX2FwcF9tZXRhZGF0YSB1cGRhdGU6dXNlcnNfYXBwX21ldGFkYXRhIGRlbGV0ZTp1c2Vyc19hcHBfbWV0YWRhdGEgY3JlYXRlOnVzZXJzX2FwcF9tZXRhZGF0YSByZWFkOnVzZXJfY3VzdG9tX2Jsb2NrcyBjcmVhdGU6dXNlcl9jdXN0b21fYmxvY2tzIGRlbGV0ZTp1c2VyX2N1c3RvbV9ibG9ja3MgY3JlYXRlOnVzZXJfdGlja2V0cyByZWFkOmNsaWVudHMgdXBkYXRlOmNsaWVudHMgZGVsZXRlOmNsaWVudHMgY3JlYXRlOmNsaWVudHMgcmVhZDpjbGllbnRfa2V5cyB1cGRhdGU6Y2xpZW50X2tleXMgZGVsZXRlOmNsaWVudF9rZXlzIGNyZWF0ZTpjbGllbnRfa2V5cyByZWFkOmNvbm5lY3Rpb25zIHVwZGF0ZTpjb25uZWN0aW9ucyBkZWxldGU6Y29ubmVjdGlvbnMgY3JlYXRlOmNvbm5lY3Rpb25zIHJlYWQ6cmVzb3VyY2Vfc2VydmVycyB1cGRhdGU6cmVzb3VyY2Vfc2VydmVycyBkZWxldGU6cmVzb3VyY2Vfc2VydmVycyBjcmVhdGU6cmVzb3VyY2Vfc2VydmVycyByZWFkOmRldmljZV9jcmVkZW50aWFscyB1cGRhdGU6ZGV2aWNlX2NyZWRlbnRpYWxzIGRlbGV0ZTpkZXZpY2VfY3JlZGVudGlhbHMgY3JlYXRlOmRldmljZV9jcmVkZW50aWFscyByZWFkOnJ1bGVzIHVwZGF0ZTpydWxlcyBkZWxldGU6cnVsZXMgY3JlYXRlOnJ1bGVzIHJlYWQ6cnVsZXNfY29uZmlncyB1cGRhdGU6cnVsZXNfY29uZmlncyBkZWxldGU6cnVsZXNfY29uZmlncyByZWFkOmhvb2tzIHVwZGF0ZTpob29rcyBkZWxldGU6aG9va3MgY3JlYXRlOmhvb2tzIHJlYWQ6YWN0aW9ucyB1cGRhdGU6YWN0aW9ucyBkZWxldGU6YWN0aW9ucyBjcmVhdGU6YWN0aW9ucyByZWFkOmVtYWlsX3Byb3ZpZGVyIHVwZGF0ZTplbWFpbF9wcm92aWRlciBkZWxldGU6ZW1haWxfcHJvdmlkZXIgY3JlYXRlOmVtYWlsX3Byb3ZpZGVyIGJsYWNrbGlzdDp0b2tlbnMgcmVhZDpzdGF0cyByZWFkOnRlbmFudF9zZXR0aW5ncyB1cGRhdGU6dGVuYW50X3NldHRpbmdzIHJlYWQ6bG9ncyByZWFkOmxvZ3NfdXNlcnMgcmVhZDpzaGllbGRzIGNyZWF0ZTpzaGllbGRzIHVwZGF0ZTpzaGllbGRzIGRlbGV0ZTpzaGllbGRzIHJlYWQ6YW5vbWFseV9ibG9ja3MgZGVsZXRlOmFub21hbHlfYmxvY2tzIHVwZGF0ZTp0cmlnZ2VycyByZWFkOnRyaWdnZXJzIHJlYWQ6Z3JhbnRzIGRlbGV0ZTpncmFudHMgcmVhZDpndWFyZGlhbl9mYWN0b3JzIHVwZGF0ZTpndWFyZGlhbl9mYWN0b3JzIHJlYWQ6Z3VhcmRpYW5fZW5yb2xsbWVudHMgZGVsZXRlOmd1YXJkaWFuX2Vucm9sbG1lbnRzIGNyZWF0ZTpndWFyZGlhbl9lbnJvbGxtZW50X3RpY2tldHMgcmVhZDp1c2VyX2lkcF90b2tlbnMgY3JlYXRlOnBhc3N3b3Jkc19jaGVja2luZ19qb2IgZGVsZXRlOnBhc3N3b3Jkc19jaGVja2luZ19qb2IgcmVhZDpjdXN0b21fZG9tYWlucyBkZWxldGU6Y3VzdG9tX2RvbWFpbnMgY3JlYXRlOmN1c3RvbV9kb21haW5zIHVwZGF0ZTpjdXN0b21fZG9tYWlucyByZWFkOmVtYWlsX3RlbXBsYXRlcyBjcmVhdGU6ZW1haWxfdGVtcGxhdGVzIHVwZGF0ZTplbWFpbF90ZW1wbGF0ZXMgcmVhZDptZmFfcG9saWNpZXMgdXBkYXRlOm1mYV9wb2xpY2llcyByZWFkOnJvbGVzIGNyZWF0ZTpyb2xlcyBkZWxldGU6cm9sZXMgdXBkYXRlOnJvbGVzIHJlYWQ6cHJvbXB0cyB1cGRhdGU6cHJvbXB0cyByZWFkOmJyYW5kaW5nIHVwZGF0ZTpicmFuZGluZyBkZWxldGU6YnJhbmRpbmcgcmVhZDpsb2dfc3RyZWFtcyBjcmVhdGU6bG9nX3N0cmVhbXMgZGVsZXRlOmxvZ19zdHJlYW1zIHVwZGF0ZTpsb2dfc3RyZWFtcyBjcmVhdGU6c2lnbmluZ19rZXlzIHJlYWQ6c2lnbmluZ19rZXlzIHVwZGF0ZTpzaWduaW5nX2tleXMgcmVhZDpsaW1pdHMgdXBkYXRlOmxpbWl0cyBjcmVhdGU6cm9sZV9tZW1iZXJzIHJlYWQ6cm9sZV9tZW1iZXJzIGRlbGV0ZTpyb2xlX21lbWJlcnMgcmVhZDplbnRpdGxlbWVudHMiLCJndHkiOiJjbGllbnQtY3JlZGVudGlhbHMifQ.V06qVp0su1yf6p6tw6k0WwKx3GKaWqovnRSP-81MKA5kyNwJc3PLLXW2H0SLu2GtSORmmPZPV9_6ogfVvRf-GzMipm-FUFmoO2TP8bShRWiu_ecSq6Hs0gBgLj5z4x3ZQSzzJ1jbA2t7kKdRknATo0vFv0HD7dSyp3H2L22Cf_6J17ZXElbJO_3EXSynRSeyeNa0U2AjAq8MbEmbAGQY8GaadN0JaFxX6AN02iZRuNyUkRLP1PhB8vAfrd2Hq05cs_nkhdMV4SuzeLtL6E3WnDCoiOqo3wf44PXRNGE_stJMJgkjF5oKdGqjZvmuxYvTqsorGYIoLaQklhjmFXSFjQ
Response - {
    "Foo": "Bar"
}

case 2:
when query param other than Foo is passed

Response 
{
    "Message": "Agreed Query Parm is not passed in the request"
}

case 3:
when wrong Bearer token is passed

Response 

    {
    "error": "Invalid token."
}

Post Flow

url - https://localhost:8124/world
Authorization code - eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6ImdlUldnekZYUERBVnhqTzlNZzROZSJ9.eyJpc3MiOiJodHRwczovL2Rldi1yOTJ1NnJzNC51cy5hdXRoMC5jb20vIiwic3ViIjoiZ29vZ2xlLW9hdXRoMnwxMTI3MTAxNTQ5NDc5NzMyNTgwODciLCJhdWQiOiJZRkFxclNJeE1sOTVYcmw3ZVVlWGxzU21zRXZVb3lEUiIsImlhdCI6MTYxNDE3NTg0NCwiZXhwIjoxNjE0MjExODQ0fQ.esydkzv_jMA4iVqEfDiNSsyaFpLDoZf_PTwdsauB9hj5KX6QxT4O_Q2KaRCVvrTjYgMM1vE0e7ASpICrG9phGXnr3Vc67Jvk762IBVPFHX9iYNwWE70UEeA0aqmb4z8Y4FU6yLjw4KNthxZCRpiMQNA7fcjZyWs4hV7-Nw5uY3GVpbKURpRF5a1cN10qEEP28yvoMWiXqVEAoOWyegRXPmIXdxy1uhpTyP4IH7UQWZzEAxn_C_9u4Uzg87v0c0uhYu34y2c5VVlIZeqj2H_xtUZ19HFAreZJYiW2lyd6u9iN8KquS9IXpMJwd3z6yPgk_6L5mU42aIOLSYVwArY1uQ

request - 
        	{
    "NFoo": "aarFfgerfgrergfwr",
    "muraliThuraka": "MuraliThuraka"
}


Response - {
    "NFoo": "aarFfgerfgrergfwr",
    "MuraliThuraka": "muraliThuraka"
}

case 2:
when empty payload is passed

Response 
{
    "Message": "payload is empty"
}

case 3:
when wrong Bearer token is passed

Response 

    {
    "error": "Invalid token."
}

Delete Flow

url - https://localhost:8124/test/{key} 

case 1:

key = status
 
 No auth0 implementation for this flow

if the key in the payload is passed in the url param 

request - 
         {
      "status": "403",
      "source": { "pointer": "/data/attributes/secretPowers" },
      "detail": "Editing secret powers is not authorized on Sundays."
    }


Response - {
    "source": {
        "pointer": "/data/attributes/secretPowers"
    },
    "detail": "Editing secret powers is not authorized on Sundays."
}

case 2:
key = statu

request - 
         {
      "status": "403",
      "source": { "pointer": "/data/attributes/secretPowers" },
      "detail": "Editing secret powers is not authorized on Sundays."
    }

Response 
{
    
    "Message": "Key is not present in url param or key is empty"
}





