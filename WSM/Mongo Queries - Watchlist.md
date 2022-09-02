---
created: 2022-08-30T16:19:31-04:00
updated: 2022-08-30T16:19:31-04:00
---
we use the status for the automated reports.  
wsm write up report:  

"reportMetadata.status": {
            "$in": ["Confirmed Callout", "Leadership Review", "Potential Callout", "StayPuft", "Top Rope", "WOZ"]
        }

watchlist report:  

"$or": [
            {
                "reportMetadata.status": {
                    "$in": [
                        "Carry Over",
                        "Confirmed Callout",
                        "Leadership Review",
                        "Potential Callout",
                        "WOZ",
                        "StayPuft",
                        "Top Rope"
                    ]
                }
            },
            {
                "reportMetadata.status": {"$in": ["Dropped", "Dropped Post Review"]},
                "reportMetadata.dateDropped": {"$gt": greater_than_date},
            },
        ],

![white_check_mark](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F2705%402x.png)![eyes](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F1f440%402x.png)![raised_hands](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F1f64c%402x.png)

[2:14](https://amzn-aws.slack.com/archives/D03UJPR5VJB/p1661883269438949)

You may also use "$or" on the query builder to query for multiple weeks.