
# Response Additional Data Network Tokens

## Structure

`ResponseAdditionalDataNetworkTokens`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network_token_available` | `String` | Optional | Indicates whether a network token is available for the specified card. |
| `network_token_bin` | `String` | Optional | The Bank Identification Number of a tokenized card, which is the first six digits of a card number. |
| `network_token_token_summary` | `String` | Optional | The last four digits of a network token. |

## Example (as JSON)

```json
{
  "networkToken.available": "networkToken.available8",
  "networkToken.bin": "networkToken.bin0",
  "networkToken.tokenSummary": "networkToken.tokenSummary4"
}
```

