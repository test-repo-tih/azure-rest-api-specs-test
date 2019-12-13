# Test Service

``` yaml
openapi-type: arm
tag: package-2020-01
```

``` yaml $(tag) == 'package-2020-01'
input-file:
- Microsoft.TestService/stable/2020-01-01/TestService.json
```

``` yaml $(multiapi)
batch:
  - tag: package-2020-01
```

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
```

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: testservice
  clear-output-folder: true
```

``` yaml $(tag) == 'package-2020-01' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2020-01-01/$(namespace)
```
