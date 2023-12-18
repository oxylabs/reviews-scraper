# Reviews Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Reviews Scraper](https://oxylabs.io/products/scraper-api/web/reviews-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any reviews website effortlessly. This brief guide explains how a Reviews Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get reviews in an HTML form by providing your own URLs to our service.

#### Python code example

The example below illustrates how you can get HTML of a [trustpilot.com] review page

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.trustpilot.com/review/www.amazon.com'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/reviews-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-US\"><head><meta charSet=\"UTF-8\"/><meta name=\"viewport\" content=\"width= ... </html>",
      "created_at": "2023-12-18 11:39:23",
      "updated_at": "2023-12-18 11:39:24",
      "page": 1,
      "url": "https://www.trustpilot.com/review/www.amazon.com",
      "job_id": "7142478451570673665",
      "status_code": 200
    }
  ]
}
```
With our Reviews Scraper, you can easily gather public data from any review-based web page. Accumulate vital book reviews, such as ratings, testimonials, or plot summaries, to evaluate the literary market and outpace your rivals. If there are any concerns or questions, feel free to reach out to our support team through live chat or send us an email at hello@oxylabs.io.
