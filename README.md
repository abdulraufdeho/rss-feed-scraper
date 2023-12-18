# RSS Feed Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [RSS Feed Scraper](https://oxylabs.io/products/scraper-api/web/rss-feed-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any RSS Feed effortlessly. This brief guide explains how a RSS Feed Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get RSS Feed results by providing your own URLs to our service. We can return the HTML for any RSS Feed page you like.

#### Python code example

The example below illustrates how you can get HTML of a RSS Feed page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://news.yahoo.com/rss/politics'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/rss-feed-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><rss xmlns:media=\"http://search.yahoo.com/mrss/\" version=\"2.0\" ... </html>",
      "created_at": "2023-12-18 11:34:34",
      "updated_at": "2023-12-18 11:34:36",
      "page": 1,
      "url": "https://news.yahoo.com/rss/politics",
      "job_id": "7142477237491672065",
      "status_code": 200
    }
  ]
}
```
With our RSS Feed Scraper, you can seamlessly pull public data from your preferred RSS Feed web pages. Gather crucial book information like author, publication date, genre, or synopses to stay updated on industry trends and keep an edge over your competitors. If you require assistance or have any queries, feel free to engage our support team via live chat or drop us an email at hello@oxylabs.io.
