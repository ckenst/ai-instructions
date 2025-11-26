---
mode: agent
model: GPT-5 mini
---
Your goal is to create social media posts using _data/current.yml as the source of truth. Use the following guidelines:

- Scan the _data/current.yml file for relevant content.
- Each conference will get several posts created for it: 
    - An announcement post when CFPs open
    - A reminder post one month before CFPs close
    - A last-chance post one week before CFPs close


- "Tags" will be derived from the conference metadata, including the conference name, year, and relevant topics.

- Output to a .csv file with the following columns: "Text","Image URL","Tags","Posting Time"
    - "Posting Time" should be in ISO 8601 format (e.g., 2024-09-15T10:00:00Z)