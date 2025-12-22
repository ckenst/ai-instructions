tools:

- Prepare newsletter script
    - prompt for the current date and/or grab current date automatically and confirm it
    - should run the identify_updates script and wait for confirmation of updates are in place
    - should run the monthly_data script and grab 3 months worth of conference data 
        - current month, next month, following month. 
        - Separate into 3 sections each with their month as a header
    - should run the status_find script to identify: 
        - CFPs that are open
        - Any conferences with discounts (early bird, group, etc) 
    - Should then create a buffer export file for promoting on social media