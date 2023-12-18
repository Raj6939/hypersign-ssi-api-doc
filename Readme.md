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


Response
  ```
      {
      "credentialDocument": {
        "@context": [
          "https://www.w3.org/2018/credentials/v1",
          {
            "hs": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/schema/sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0:"
          },
          {
            "name": "hs:name"
          },
          {
            "rollNo": "hs:rollNo"
          },
          "https://w3id.org/security/suites/ed25519-2020/v1"
        ],
        "id": "vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
        "type": [
          "VerifiableCredential",
          "Degree "
        ],
        "expirationDate": "2027-12-10T18:30:00Z",
        "issuanceDate": "2023-12-18T13:31:00Z",
        "issuer": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
        "credentialSubject": {
          "name": "Raj",
          "rollNo": 20,
          "id": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu"
        },
        "credentialSchema": {
          "id": "sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0",
          "type": "JsonSchemaValidator2018"
        },
        "credentialStatus": {
          "id": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/credential/vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
          "type": "CredentialStatusList2017"
        },
        "proof": {
          "type": "Ed25519Signature2020",
          "created": "2023-12-18T13:32:40Z",
          "verificationMethod": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
          "proofPurpose": "assertionMethod",
          "proofValue": "z3dW8HXSzSQv2khSAAHZSNa6WC16YR6dpQFAxvwN8NMvkfxFsKKxXfDpNJiZbnHUwNUjv7Dq41zWmcsU7xfiyiLg3"
        }
      },
      "credentialStatus": {
        "claim": {
          "id": "vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
          "currentStatus": "Live",
          "statusReason": "Credential is active"
        },
        "issuer": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
        "issuanceDate": "2023-12-18T13:31:00Z",
        "expirationDate": "2027-12-10T18:30:00Z",
        "credentialHash": "3c55af63c626dbfde387fcb29eee595c4855125bdfd990b69d3123985a23317e"
      },
      "persist": true
    }
```

  5. Create Verifiable Presentation

  Method: POST

  URL:

  Body:

  ```
  {
  "credentialDocuments": [
    {
      "@context": [
        "https://www.w3.org/2018/credentials/v1",
        {
          "hs": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/schema/sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0:"
        },
        {
          "name": "hs:name"
        },
        {
          "rollNo": "hs:rollNo"
        },
        "https://w3id.org/security/suites/ed25519-2020/v1"
      ],
      "id": "vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
      "type": [
        "VerifiableCredential",
        "Degree "
      ],
      "expirationDate": "2027-12-10T18:30:00Z",
      "issuanceDate": "2023-12-18T13:31:00Z",
      "issuer": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
      "credentialSubject": {
        "name": "Raj",
        "rollNo": 20,
        "id": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu"
      },
      "credentialSchema": {
        "id": "sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0",
        "type": "JsonSchemaValidator2018"
      },
      "credentialStatus": {
        "id": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/credential/vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
        "type": "CredentialStatusList2017"
      },
      "proof": {
        "type": "Ed25519Signature2020",
        "created": "2023-12-18T13:32:40Z",
        "verificationMethod": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
        "proofPurpose": "assertionMethod",
        "proofValue": "z3dW8HXSzSQv2khSAAHZSNa6WC16YR6dpQFAxvwN8NMvkfxFsKKxXfDpNJiZbnHUwNUjv7Dq41zWmcsU7xfiyiLg3"
      }
    }
  ],
  "holderDid": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu",
  "challenge": "Raj",
  "domain": "example.com"
}
```

Response

```
{
  "presentation": {
    "@context": [
      "https://www.w3.org/2018/credentials/v1",
      "https://w3id.org/security/suites/ed25519-2020/v1"
    ],
    "type": [
      "VerifiablePresentation"
    ],
    "verifiableCredential": [
      {
        "@context": [
          "https://www.w3.org/2018/credentials/v1",
          {
            "hs": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/schema/sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0:"
          },
          {
            "name": "hs:name"
          },
          {
            "rollNo": "hs:rollNo"
          },
          "https://w3id.org/security/suites/ed25519-2020/v1"
        ],
        "id": "vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
        "type": [
          "VerifiableCredential",
          "Degree"
        ],
        "expirationDate": "2027-12-10T18:30:00Z",
        "issuanceDate": "2023-12-18T13:31:00Z",
        "issuer": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9",
        "credentialSubject": {
          "name": "Raj",
          "rollNo": 20,
          "id": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu"
        },
        "credentialSchema": {
          "id": "sch:hid:testnet:zEinwkuP5XUtU2AmArh4rqbCLbwzZRebBQzitCSafiiSG:1.0",
          "type": "JsonSchemaValidator2018"
        },
        "credentialStatus": {
          "id": "https://api.jagrat.hypersign.id/hypersign-protocol/hidnode/ssi/credential/vc:hid:testnet:zDm9qhMncSGnudGYquzz3mGfV8yahS4yKcWmeWTb5pcxe",
          "type": "CredentialStatusList2017"
        },
        "proof": {
          "type": "Ed25519Signature2020",
          "created": "2023-12-18T13:32:40Z",
          "verificationMethod": "did:hid:testnet:z6y1cC2BCFw2ZoAcxcSZNAFE87xSQNqoGTAR4xxoWFD9#key-1",
          "proofPurpose": "assertionMethod",
          "proofValue": "z3dW8HXSzSQv2khSAAHZSNa6WC16YR6dpQFAxvwN8NMvkfxFsKKxXfDpNJiZbnHUwNUjv7Dq41zWmcsU7xfiyiLg3"
        }
      }
    ],
    "id": "vp:hid:testnet:z6hkcEGWy4yy6S51pMqZb6Ds6imws4Ukm5rApyv4yxJdj",
    "holder": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu",
    "proof": {
      "type": "Ed25519Signature2020",
      "created": "2023-12-18T13:37:24Z",
      "verificationMethod": "did:hid:testnet:z2ikbFoMbenw3ajCd5jVzrncCXycdkbeAWte3nLpdrjHu#key-1",
      "proofPurpose": "authentication",
      "challenge": "Raj",
      "proofValue": "z4iNMU6t32Y9cjdYVmV5npQWXxJVGdqtzb4S8Wvf3RzziiEbvTnmpQ7UbGNFc4wdR6yVZR915TFVkHiugUf6mdpT4"
    }
  }
}
```
  
