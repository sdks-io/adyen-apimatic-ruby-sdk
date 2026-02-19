
# Checkout Network Token Option

## Structure

`CheckoutNetworkTokenOption`

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

