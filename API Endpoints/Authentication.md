---
label: "Authentication"
icon: shield-check
order: 100
---

# Authentication

All API requests require authentication using your facility's API key.

## Obtaining Your API Key

1. Navigate to **FIR Management** > **Web Configuration**
2. Locate the **API Keys** section
3. Copy your facility's API key
4. Keep this key secure - do not share it publicly or commit it to version control

## Using Your API Key

Include your API key in the request header with each API call.

||| Header Parameter Name
api_key
|||

## Example Requests

### cURL
```bash
curl -H "api_key: your_api_key_here" \
  https://vatcar.net/api/v2/facility/roster
```

### JavaScript (Fetch API)
```javascript
fetch('https://vatcar.net/api/v2/facility/roster', {
  headers: {
    'api_key': 'your_api_key_here'
  }
})
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error('Error:', error));
```

### Python (Requests)
```python
import requests

headers = {
    'api_key': 'your_api_key_here'
}

response = requests.get('https://vatcar.net/api/v2/facility/roster', headers=headers)
data = response.json()
print(data)
```

### PHP
```php
<?php
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, "https://vatcar.net/api/v2/facility/roster");
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTPHEADER, array(
    'api_key: your_api_key_here'
));

$response = curl_exec($ch);
curl_close($ch);

$data = json_decode($response, true);
print_r($data);
?>
```

## Error Responses

### HTTP Status Codes

| Status Code | Description | Solution |
|-------------|-------------|----------|
| 401 | Invalid or missing API key | Verify your API key is correct and included in the header |
| 403 | Access denied for this resource | Contact VATCAR staff to verify your facility's API permissions |
| 429 | Rate limit exceeded | Wait before making additional requests |
| 500 | Internal server error | Contact VATCAR support if the issue persists |

### Invalid API Key Response

When an invalid API key is provided, the API returns an error response with details:

```json
{
  "error": "Invalid API key.",
  "api_key": ""
}
```

The response includes:
- **error**: Error message indicating the API key is invalid
- **api_key**: The API key that was provided (for debugging purposes)

If you receive this error, verify that:
1. You copied the complete API key from the FIR Management page
2. There are no extra spaces or characters in your API key
3. Your API key hasn't been regenerated or revoked

## Best Practices

- **Never expose your API key** in client-side code or public repositories
- **Store API keys securely** using environment variables or secure configuration files
- **Implement error handling** to gracefully manage failed requests
- **Respect rate limits** to ensure API availability for all facilities
- **Use HTTPS** for all API requests (enforced by default)