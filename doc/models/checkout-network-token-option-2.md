
# Checkout Network Token Option 2

The object that contains the details for forwarding a network token.

## Structure

`CheckoutNetworkTokenOption2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `include_cryptogram` | `TrueClass \| FalseClass` | Optional | Set to **true** to enable forwarding network token cryptograms. |
| `use_network_token` | `TrueClass \| FalseClass` | Optional | Set to **true** to forward the network token for a card. |

## Example (as JSON)

```json
{
  "includeCryptogram": false,
  "useNetworkToken": false
}
```

