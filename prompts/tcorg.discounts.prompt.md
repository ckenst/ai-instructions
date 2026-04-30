Using `_data/current.yml`, prepare a list of conferences with discount pricing for the entire year.

Discounts mean the `status` field contains any of:
- Early Bird
- Super Early Bird
- Blind Bird
- Sale

Format each item like this:

[**Conference Title**](conference url)  
**Location:** location  
**Dates:** dates  
**Status:** rendered status text

Rules:
- Use the `url` field for the title link.
- Strip HTML tags from status and show only readable text.
- Keep non-discount status text if it appears in the same status field, but only include conferences whose status contains a discount term.
