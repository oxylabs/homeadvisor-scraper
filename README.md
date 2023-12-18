# Homeadvisor Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Homeadvisor Scraper](https://oxylabs.io/products/scraper-api/web/homeadvisor?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Homeadvisor website effortlessly. This brief guide explains how an Homeadvisor Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Homeadvisor results by providing your own URLs to our service. We can return the HTML for any Homeadvisor page you like.

#### Python code example

The example below illustrates how you can get HTML of Homeadvisor page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.homeadvisor.com/task.windows-install-or-replace.46355.html?sequence=0'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/homeadvisor-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n<!DOCTYPE html>\n<!--[if IE 9]>       <html xmlns=\"http://www.w3.org/19 ... </html>",
      "created_at": "2023-12-18 11:10:28",
      "updated_at": "2023-12-18 11:10:30",
      "page": 1,
      "url": "https://www.homeadvisor.com/task.windows-install-or-replace.46355.html?sequence=0",
      "job_id": "7142471174910459905",
      "status_code": 200
    }
  ]
}
```
With our Homeadvisor Scraper, you can seamlessly extract public data from any Homeadvisor webpage. Gather necessary information such as service providers' ratings, customer reviews, service descriptions, and pricing details to understand the market trends and get a competitive edge. If you require assistance, our support team is willing to help through live chat or you can email us at hello@oxylabs.io.