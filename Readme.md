## Contracts

This directory contains the **OpenAPI contracts** for the **authentication** and **product** APIs.

The OpenAPI contracts are used to **validate the API endpoints and their responses** ensuring that implements matches the defined api specification.

---

## Contract Validation 

The contracts are validated by the **Validate** job defined in the `.github/workflows/contracts.yml`

---

## Validation Tool

To validate the Openapi contracts we are using the **[swagger-cli](https://swagger.io/tools/swagger-cli/)** package.

---

## Installing swagger-cli

```bash
npm install -g swagger-cli
```

---

## Validating the contracts

```bash
swagger-cli validate openapi.yml
```
This command:
- Fails if the OpenAPI contract is invalid
- Fails if there are broken **$ref** references.
- Passes only if the contract is valid and has no broken **$ref** references. 