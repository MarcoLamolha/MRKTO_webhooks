# MRKTO_webhooks

## Sending a request to a webhook URL

### Using `curl`

To send a request to a webhook URL using `curl`, you can use the following command:

```sh
curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1", "key2":"value2"}' https://your-webhook-url.com
```

This command sends a POST request with JSON data to the specified webhook URL.

### Using Python

To send a request to a webhook URL using Python, you can use the `requests` library. Here is an example script:

```python
import requests
import json

url = 'https://your-webhook-url.com'
data = {
    'key1': 'value1',
    'key2': 'value2'
}

response = requests.post(url, data=json.dumps(data), headers={'Content-Type': 'application/json'})

print(response.status_code)
print(response.text)
```

This script sends a POST request with JSON data to the specified webhook URL and prints the response status code and text.
