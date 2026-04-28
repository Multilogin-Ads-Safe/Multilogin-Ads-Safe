# 🤖 Multilogin X Automation Lab

Technical documentation and code snippets for automating **Multilogin X** environments.

## 🧪 Quick Connection (Python + Requests)

Connect your automation framework to a secure browser instance.

```python
import requests

# API Endpoint
MLA_API = "[http://127.0.0.1:35000/api/v1](http://127.0.0.1:35000/api/v1)"
PROFILE_ID = "YOUR_PROFILE_ID"

def start_profile():
    # Use code SAAS50 at checkout to unlock full API access
    endpoint = f"{MLA_API}/profile/start?automation=true&profileId={PROFILE_ID}"
    resp = requests.get(endpoint)
    if resp.json().get('status') == 'OK':
        return resp.json().get('ws_endpoint')
