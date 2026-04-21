# Numerology API - DivineAPI

> Free **Numerology API** for developers. 15+ REST endpoints covering life path, destiny, soul urge and personality numbers, Loshu grid, Chaldean numerology, yearly predictions and mobile number analysis. Plain JSON over HTTPS, 25 languages, no SDK required.

[![Get API Key](https://img.shields.io/badge/Get%20API%20Key-cb22e6?style=for-the-badge&logoColor=white)](https://divineapi.com/register)
[![Live Docs](https://img.shields.io/badge/Live%20Docs-4F46E5?style=for-the-badge&logoColor=white)](https://developers.divineapi.com/numerology-apis)
[![API Status](https://img.shields.io/badge/API%20Status-10b981?style=for-the-badge&logoColor=white)](https://status.divineapi.com)
[![14-Day Free Trial](https://img.shields.io/badge/14--Day%20Free%20Trial-039BE5?style=for-the-badge&logoColor=white)](https://divineapi.com/register)
[![Postman](https://img.shields.io/badge/Run%20in%20Postman-FF6C37?style=for-the-badge&logoColor=white)](https://documenter.getpostman.com/view/26759678/2sBXitCnDX)

<p align="center">
  <img src="https://developers.divineapi.com/public/assets/web/images/divineIcon.svg" alt="DivineAPI, Numerology API for developers" width="120" />
</p>

---

## What is the Numerology API?

The **Numerology API** by DivineAPI is a suite of 15+ REST endpoints for numerology calculations. Give a full name and birth date, get back the complete numerology profile: life path, expression/destiny, soul urge, personality, birthday numbers, plus Loshu grid patterns, Chaldean-system readings, yearly predictions, gemstone remedies and mobile-number analysis. Plain JSON over HTTPS, 25 languages, no SDK required.

Part of the broader [DivineAPI platform](https://github.com/DivineAPI/astrology-api) (200+ astrology, horoscope, tarot and numerology endpoints).

## Why choose DivineAPI's Numerology API?

- **15+ REST endpoints** covering Pythagorean and Chaldean numerology
- **Core Numbers in one call**: life path, expression, soul urge, personality, birthday
- **Loshu (magic square) grid** analysis with missing-number and repeating-number insights
- **Mobile number analysis** and new-number suggestions based on birth data
- **Yearly predictions** and gemstone recommendations grounded in numerology
- **25-language output**: English, Hindi, Spanish, French, Arabic, Chinese, and more
- **No SDK lock-in**: plain JSON over HTTPS, works with every language
- **Live status page**: uptime monitored at [status.divineapi.com](https://status.divineapi.com)

## All endpoints in the Numerology API

### Core Numerology Profile

| Endpoint | Docs |
|---|---|
| Core Numbers | [link](https://developers.divineapi.com/numerology-apis/core-numbers) |
| Name Number | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/name-number) |
| Birthday Number | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/birthday-number) |

### Loshu Grid & Number Patterns

| Endpoint | Docs |
|---|---|
| Loshu Grid | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/loshu-grid-api) |
| Missing Numbers | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/missing-numbers) |
| Repeating Numbers | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/repeating-numbers) |
| Driver and Conductor Number | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/driver-and-conductor-number) |

### Number Arrows & Insights

| Endpoint | Docs |
|---|---|
| Two Number Arrow | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/two-number-arrow) |
| Three Number Arrow | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/three-number-arrow) |
| Zodiac Planet Number | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/zodiac-planet-number) |

### Predictions & Remedies

| Endpoint | Docs |
|---|---|
| Luck Numerology | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/luck-numerology) |
| Yearly Prediction | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/yearly-prediction) |
| Gemstone Suggestion | [link](https://developers.divineapi.com/numerology-apis/chaldean-numerology/gemstone-suggestion) |

### Mobile Numerology

| Endpoint | Docs |
|---|---|
| New Mobile Number | [link](https://developers.divineapi.com/numerology-apis/mobile-numerology/new-mobile-number) |
| Analyze Mobile Number | [link](https://developers.divineapi.com/numerology-apis/mobile-numerology/analyze-mobile-number) |

Full reference, request/response samples, and live "try-it" console → **[developers.divineapi.com/numerology-apis](https://developers.divineapi.com/numerology-apis)**

---

## Quick start

1. **Get your API key** → [divineapi.com/register](https://divineapi.com/register) (14-day free trial, no credit card)
2. **Make your first call** - see the walkthrough below
3. **Browse all endpoints** → [developers.divineapi.com/numerology-apis](https://developers.divineapi.com/numerology-apis)

---

## Walkthrough: Core Numbers

The flagship endpoint. Submit a name and birth date, get back all core numerology numbers (life path, expression, soul urge, personality, birthday) in a single call, each with a full interpretive description.

```http
POST https://astroapi-4.divineapi.com/numerology/v1/core-numbers
```

Authenticate with a Bearer token in the `Authorization` header **and** pass `api_key` in the request body (both required).

### Request body

| Parameter | Type | Required | Description | Example |
|---|---|:---:|---|---|
| `api_key` | string | ✓ | Your DivineAPI key | `YOUR_API_KEY` |
| `full_name` | string | ✓ | Name to analyze | `Amit Kumar` |
| `day` | integer | ✓ | Date of birth (day) | `24` |
| `month` | integer | ✓ | Month of birth | `5` |
| `year` | integer | ✓ | Year of birth | `1990` |
| `gender` | string | ✓ | Gender | `male` |
| `method` | string | ✓ | Numerology system: `chaldean` or `pythagorean` | `chaldean` |
| `lan` | string | - | Language code (default `en`) | `en` |

Full docs → **[developers.divineapi.com/numerology-apis/core-numbers](https://developers.divineapi.com/numerology-apis/core-numbers)**

### Sample response

```json
{
  "success": 1,
  "data": {
    "life_path_number": {
      "name": "Life Path Number",
      "number": 9,
      "description": "As a Life Path 9, you are a natural humanitarian. You possess a deep concern for the well-being of others, often driven by empathy and compassion..."
    },
    "expression_number": {
      "name": "Expression Number",
      "number": 5,
      "description": "..."
    },
    "soul_urge_number": {
      "name": "Soul Urge Number",
      "number": 3,
      "description": "..."
    },
    "personality_number": {
      "name": "Personality Number",
      "number": 2,
      "description": "..."
    },
    "birthday_number": {
      "name": "Birthday Number",
      "number": 6,
      "description": "..."
    }
    // ... plus maturity number, balance number, heart's desire and more
  }
}
```

---

## Code examples

### cURL

```bash
curl -X POST "https://astroapi-4.divineapi.com/numerology/v1/core-numbers" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  --data-urlencode "api_key=YOUR_API_KEY" \
  --data-urlencode "full_name=Amit Kumar" \
  --data-urlencode "day=24" \
  --data-urlencode "month=5" \
  --data-urlencode "year=1990" \
  --data-urlencode "gender=male" \
  --data-urlencode "method=chaldean"
```

### Python (requests)

```python
import requests

url = "https://astroapi-4.divineapi.com/numerology/v1/core-numbers"

headers = {
    "Authorization": "Bearer YOUR_API_KEY",
    "Content-Type": "application/x-www-form-urlencoded",
}

payload = {
    "api_key":   "YOUR_API_KEY",
    "full_name": "Amit Kumar",
    "day":       24,
    "month":     5,
    "year":      1990,
    "gender":    "male",
    "method":    "chaldean",
}

response = requests.post(url, headers=headers, data=payload)
print(response.json())
```

### JavaScript (browser, fetch)

```javascript
const url = "https://astroapi-4.divineapi.com/numerology/v1/core-numbers";

const body = new URLSearchParams({
  api_key:   "YOUR_API_KEY",
  full_name: "Amit Kumar",
  day: 24, month: 5, year: 1990,
  gender: "male",
  method: "chaldean",
});

const response = await fetch(url, {
  method: "POST",
  headers: {
    "Authorization": "Bearer YOUR_API_KEY",
    "Content-Type":  "application/x-www-form-urlencoded",
  },
  body,
});

const data = await response.json();
console.log(data);
```

### Node.js (fetch, Node 18+)

```javascript
// Node.js 18+ ships with fetch built-in, no dependencies needed.

async function getCoreNumbers() {
  const url = "https://astroapi-4.divineapi.com/numerology/v1/core-numbers";

  const body = new URLSearchParams({
    api_key:   "YOUR_API_KEY",
    full_name: "Amit Kumar",
    day: 24, month: 5, year: 1990,
    gender: "male",
    method: "chaldean",
  });

  const res = await fetch(url, {
    method: "POST",
    headers: {
      "Authorization": "Bearer YOUR_API_KEY",
      "Content-Type":  "application/x-www-form-urlencoded",
    },
    body,
  });

  const data = await res.json();
  console.log(data);
}

getCoreNumbers();
```

### PHP (curl)

```php
<?php
$url = "https://astroapi-4.divineapi.com/numerology/v1/core-numbers";

$payload = http_build_query([
    "api_key"   => "YOUR_API_KEY",
    "full_name" => "Amit Kumar",
    "day"       => 24,
    "month"     => 5,
    "year"      => 1990,
    "gender"    => "male",
    "method"    => "chaldean",
]);

$ch = curl_init($url);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, $payload);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTPHEADER, [
    "Authorization: Bearer YOUR_API_KEY",
    "Content-Type: application/x-www-form-urlencoded",
]);

$response = curl_exec($ch);
curl_close($ch);

echo $response;
```

### Go (net/http)

```go
package main

import (
    "fmt"
    "io"
    "net/http"
    "net/url"
    "strings"
)

func main() {
    endpoint := "https://astroapi-4.divineapi.com/numerology/v1/core-numbers"

    form := url.Values{}
    form.Set("api_key",   "YOUR_API_KEY")
    form.Set("full_name", "Amit Kumar")
    form.Set("day",       "24")
    form.Set("month",     "5")
    form.Set("year",      "1990")
    form.Set("gender",    "male")
    form.Set("method",    "chaldean")

    req, _ := http.NewRequest("POST", endpoint, strings.NewReader(form.Encode()))
    req.Header.Set("Authorization", "Bearer YOUR_API_KEY")
    req.Header.Set("Content-Type",  "application/x-www-form-urlencoded")

    resp, err := http.DefaultClient.Do(req)
    if err != nil {
        panic(err)
    }
    defer resp.Body.Close()

    body, _ := io.ReadAll(resp.Body)
    fmt.Println(string(body))
}
```

---

## Other APIs by DivineAPI

[![Astrology API (hub)](https://img.shields.io/badge/Astrology%20API%20(hub)-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/astrology-api)
[![Kundali API](https://img.shields.io/badge/Kundali%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/kundali-api)
[![Birth Chart API](https://img.shields.io/badge/Birth%20Chart%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/birth-chart-api)
[![Panchang API](https://img.shields.io/badge/Panchang%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/panchang-api)
[![Horoscope API](https://img.shields.io/badge/Horoscope%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/horoscope-api)
[![Daily Tarot](https://img.shields.io/badge/Daily%20Tarot-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/daily-tarot)
[![Yes or No Tarot](https://img.shields.io/badge/Yes%20or%20No%20Tarot-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/yes-or-no-tarot)
[![Fortune Cookie](https://img.shields.io/badge/Fortune%20Cookie-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/fortune-cookie)
[![Coffee Cup Reading](https://img.shields.io/badge/Coffee%20Cup%20Reading-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/coffee-cup-reading)

---

## Resources

- **Full documentation** → [developers.divineapi.com/numerology-apis](https://developers.divineapi.com/numerology-apis)
- **Parent platform README** → [github.com/DivineAPI/astrology-api](https://github.com/DivineAPI/astrology-api)
- **API status** → [status.divineapi.com](https://status.divineapi.com)
- **Postman collection** → [Run in Postman](https://documenter.getpostman.com/view/26759678/2sBXitCnDX)
- **Changelog** → [developers.divineapi.com/changelog](https://developers.divineapi.com/changelog)
- **Support** → [admin@divineapi.com](mailto:admin@divineapi.com)

---

## License & Usage

Code samples on this page are free to copy into your own projects, no attribution required. Marketing copy, logos, and the **DivineAPI** name are © 2026 DivineAPI, all rights reserved.

For the terms that govern the API service itself, see [divineapi.com/terms](https://divineapi.com/terms).

## Contact

Questions, feature requests or partnership enquiries → **[admin@divineapi.com](mailto:admin@divineapi.com)**
