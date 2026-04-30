Using `_data/current.yml`, prepare a list of all conferences happening in [MONTH].

Include conferences whose date range overlaps [MONTH].

Format each item like this:

[**Conference Title**](conference url)  
**Location:** location  
**Dates:** dates  
**Status:** rendered status text

Rules:
- Use the `url` field for the conference title link.
- Bold the labels `Location`, `Dates`, and `Status`.
- Convert any HTML status links into plain rendered text only.
- If no status is listed, leave off the Status line.
