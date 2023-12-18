**OAUTH**
Get Access Token by calling this api by passing secret-kay-api

```
POST https://api.entity.hypersign.id/api/v1/app/oauth
Headers:
  - Content-Type: application/json
  - X-Api-Secret-Key: your-secret-key-api
```


**DID Operations**
1. Create DID


   Method: POST
   
   URL: https://api.entity.hypersign.id/api/v1/did/create
   
   body:
   ```
   {
    "namespace": "testnet"
   }
   ```
   
   Response:
   ```
        {
       "did": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
       "registrationStatus": "UNREGISTRED",
       "metaData": {
         "didDocument": {
           "@context": [
             "https://www.w3.org/ns/did/v1"
           ],
           "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
           "controller": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
           ],
           "alsoKnownAs": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
           ],
           "verificationMethod": [
             {
               "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
               "type": "Ed25519VerificationKey2020",
               "controller": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
               "publicKeyMultibase": "z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
               "blockchainAccountId": ""
             }
           ],
           "authentication": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
           ],
           "assertionMethod": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
           ],
           "keyAgreement": [],
           "capabilityInvocation": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
           ],
           "capabilityDelegation": [
             "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
           ],
           "service": []
         }
       }
     }
```

2. Register DID

   Method: POST

   URL: https://api.entity.hypersign.id/api/v1/did/register

   body:

   ```
         {
            "didDocument": {
                "@context": [
                  "https://www.w3.org/ns/did/v1"
                ],
                "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
                "controller": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
                ],
                "alsoKnownAs": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
                ],
                "verificationMethod": [
                  {
                    "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
                    "type": "Ed25519VerificationKey2020",
                    "controller": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
                    "publicKeyMultibase": "z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
                    "blockchainAccountId": ""
                  }
                ],
                "authentication": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
                ],
                "assertionMethod": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
                ],
                "keyAgreement": [],
                "capabilityInvocation": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
                ],
                "capabilityDelegation": [
                  "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
                ],
                "service": []
              },
              "verificationMethodId":"did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
          }
   ```

Response

   ```
         {
           "did": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
           "registrationStatus": "COMPLETED",
           "transactionHash": "B8C6FDFED208795D1D3C3AA712160BD8406C48048A937B96E29B48DAA3DC63E9",
           "metaData": {
             "didDocument": {
               "@context": [
                 "https://www.w3.org/ns/did/v1"
               ],
               "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
               "controller": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
               ],
               "alsoKnownAs": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9"
               ],
               "verificationMethod": [
                 {
                   "id": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
                   "type": "Ed25519VerificationKey2020",
                   "controller": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
                   "publicKeyMultibase": "z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
                   "blockchainAccountId": ""
                 }
               ],
               "authentication": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
               ],
               "assertionMethod": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
               ],
               "keyAgreement": [],
               "capabilityInvocation": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
               ],
               "capabilityDelegation": [
                 "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1"
               ],
               "service": []
             }
           }
         }
   ```

  3. Create Schema for credetnial
  Create schema here https://entity.hypersign.id/#/studio/playground/dashboard at entity studio and copy the schema Id

  4. Issue Credential for above copied schema

  Method: POST

  URL:https://api.entity.hypersign.id/api/v1/credential/issue

  Body:

  ```
    {
      "schemaId": "string",             //Schema ID copied above
      "subjectDid": "string",           // DID of the Subject
      "issuerDid": "string",            // Issuer DID
      "expirationDate": "2027-12-10T18:30:00.000Z",  //Add expiry according to your requirement
      "fields": {
        "name": "value"                 //for value you can enter name of the Subject
      },
      "namespace": "testnet",
      "verificationMethodId": "{issuerDID}#key-1",   //Issuer DID and append #key-1 at last
      "persist": true,
      "registerCredentialStatus": true
    }
```
  
   
