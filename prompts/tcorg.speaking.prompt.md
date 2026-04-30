Using `_data/current.yml`, prepare a list of speaking opportunities for the entire year.

Speaking opportunities mean the `status` field contains either:
- CFP
- Speak

Format each item like this:

[**Conference Title**](conference url)  
**Location:** location  
**Dates:** dates  
**Status:** rendered status text

Rules:
- Use the `url` field for the title link.
- Strip HTML tags from status and show only readable text.
- Include the full readable status, even when it also mentions registration or pricing.
