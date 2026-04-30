---
name: conference-list-generator
description: Generate monthly, discount, and speaking opportunity conference lists from testingconferences.github.io `_data/current.yml`.
---

# Conference List Generator

Use this skill when asked to generate reusable conference lists from `_data/current.yml`.

## Source

Read `_data/current.yml`. Each entry may include:

- `name`
- `location`
- `dates`
- `url`
- `status`

## Output Format

For each matching conference:

[**Conference Title**](conference url)  
**Location:** location  
**Dates:** dates  
**Status:** rendered status text

Omit `Status` when the user asks to leave off missing statuses.

## Rendering Rules

- Title must link to the entry’s `url`.
- Bold the labels `Location`, `Dates`, and `Status`.
- Convert HTML in `status` into rendered text.
- Remove `<a>` tags while preserving their visible text.
- Do not include status links unless explicitly requested.
- Preserve date and location text exactly as listed.

## Filters

Monthly:
Include entries where `dates` contains the requested month name. This includes date ranges spanning into that month.

Discounts:
Include entries where `status` contains `Early Bird`, `Super Early Bird`, `Blind Bird`, or `Sale`, case-insensitive.

Speaking Opportunities:
Include entries where `status` contains `CFP` or `Speak`, case-insensitive.

## Helpful Ruby Extractor

Use Ruby YAML parsing rather than ad hoc manual scanning when possible.

```ruby
require "yaml"

data = YAML.load_file("_data/current.yml")

def rendered_status(status)
  status.to_s
    .gsub(/<a[^>]*>/, "")
    .gsub(%r{</a>}, "")
    .gsub(/\s+/, " ")
    .strip
end
