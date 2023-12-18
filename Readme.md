**OAUTH**
Get Access Token by calling this api by passing secret-kay-api



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
  
   
