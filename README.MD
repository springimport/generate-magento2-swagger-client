# How generate Swagger API client for Magento 2

1. Install Swagger Codepen.
https://github.com/swagger-api/swagger-codegen

[How to install Maven on Windows](https://www.mkyong.com/maven/how-to-install-maven-in-windows/)

2. Configure swagger
https://github.com/swagger-api/swagger-codegen/issues/974


Example of `config.json`
```json
{
    "composerVendorName": "springimport",
    "composerProjectName": "swagger-magento2-client",
    "variableNamingConvention": "camelCase",
    "invokerPackage": "SpringImport\\Swagger\\Magento2\\Client"
}
```

Example generate command
```
java -jar bin/swagger-codegen-cli.jar generate -i tmp/schema/schema.json -l php -o tmp/generation/php_api_client -c ./config.json
```
OR (from latest Magento 2.2 directly)
```
java -jar bin/swagger-codegen-cli.jar generate -i http://devdocs.magento.com/swagger/schemas/latest-2.2.schema.json -l php -o tmp/generation/php_api_client-magento-2.2-latest -c ./config.json
```

### Ready for use

Magneto 2 SwaggerClient

https://github.com/springimport/swagger-magento2-client