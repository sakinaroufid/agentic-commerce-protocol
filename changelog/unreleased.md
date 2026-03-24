## Fix type mismatch for FulfillmentOption monetary fields

Corrected `subtotal`, `tax`, and `total` in `FulfillmentOptionShipping` and
`FulfillmentOptionDigital` from `string` to `integer` in the OpenAPI spec.
The JSON Schema already defined these as `integer`, and all examples use
integer values (e.g. `100` for $1.00). This aligns the OpenAPI spec with the
canonical JSON Schema and existing examples.

### Changes
- Changed `subtotal`, `tax`, `total` type from `string` to `integer` in `FulfillmentOptionShipping`
- Changed `subtotal`, `tax`, `total` type from `string` to `integer` in `FulfillmentOptionDigital`

### Files Updated
- `spec/openapi/openapi.agentic_checkout.yaml`
