pipeline {
  agent any
  stages {
    stage('test1') {
      steps {
        sh 'echo "hello world!"'
      }
    }
    stage('k8s') {
      steps {
        withKubeConfig(serverUrl: 'https://16.178.115.5:6443', credentialsId: 'admin', caCertificate: '-----BEGIN CERTIFICATE----- MIIDvjCCAqagAwIBAgIUHejB0KDRRkrp6ile8wlIBNzFMbMwDQYJKoZIhvcNAQEL BQAwZTELMAkGA1UEBhMCQ04xEDAOBgNVBAgTB0JlaWppbmcxEDAOBgNVBAcTB0Jl aWppbmcxDDAKBgNVBAoTA2s4czEPMA0GA1UECxMGc3lzdGVtMRMwEQYDVQQDEwpr dWJlcm5ldGVzMB4XDTE4MDUyOTA3MTUwMFoXDTIzMDUyODA3MTUwMFowZTELMAkG A1UEBhMCQ04xEDAOBgNVBAgTB0JlaWppbmcxEDAOBgNVBAcTB0JlaWppbmcxDDAK BgNVBAoTA2s4czEPMA0GA1UECxMGc3lzdGVtMRMwEQYDVQQDEwprdWJlcm5ldGVz MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAusgmQmtNZeLlXPrBG70H nXe4WWlIeH+O5gKrflNReJcR5lqJJT3dvetOiyOERHQoPfWYCwL3fDQ3OiZychR8 idJoQ1GR1dLzJtP+vDc/Zds3k82eUWoY9RS5u9ZgwvPDTjxnnIQmnnQqZvxChaZ8 54DkBGoeYQ1bIj9bmGILWXgdRRDDJ2M9YvKEn5Z1vTBE0jRcWL+l/LS0LWsUfQ8W 2an/SJXZcJBG8UEMgAewLFGhsfKfim8jv44VXXBdb63rWCH8AnVdpQs760bW1nOC 6Jit6emlsRabdrijV7+sLRgPSgRq2ZB2vn/KIJXVhaykw3xwiabsE5w+4JsZwx3K owIDAQABo2YwZDAOBgNVHQ8BAf8EBAMCAQYwEgYDVR0TAQH/BAgwBgEB/wIBAjAd BgNVHQ4EFgQUWivWZ7BGA5bUG4cU4OM3MnAtdBIwHwYDVR0jBBgwFoAUWivWZ7BG A5bUG4cU4OM3MnAtdBIwDQYJKoZIhvcNAQELBQADggEBAEGby8dawJqL2WQXvkMn JzOTXa+O9m0HGiPZTyhn4u1WCH4UProOVO3cOBp6OL0Ahs00Ij3ltT3ETfNtfLQo 0dQ1mstoL8HHudETFML0kLyce+1SuzRPSwvEh2ljE1Bl0xxdl7oanq9hHMHp8meX DMbHvVkegZXlmPC93IljxeI++zMT9vN/NL6vyZF1jNw89jDTJqUK21Vt/3dh1asP 6hlH83IejD1jA66U1l6kD+l/JdV2eorfMEhAICBikX+hlySFlQm0FpEhDFXY3tKI 8hareKujDl2hFx43Lub/H4hXQAfcCfVdWERh/oWK8yWnJV1Uk0sPTFJ0A6DS4078 BqE= -----END CERTIFICATE-----') {
          sh 'kubectl get pod'
        }

      }
    }
  }
}