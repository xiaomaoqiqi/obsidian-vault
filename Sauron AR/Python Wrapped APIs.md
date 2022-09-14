---
created: 2022-09-01T18:30:05-04:00
updated: 2022-09-02T17:14:37-04:00
---

SecDevOps has added a set of new APIs to the [SauronPythonClient](https://code.amazon.com/packages/SauronPythonClient/trees/mainline) package related to watchlist email reports! This package is a Python client for communicating with the [Sauron v3](https://w.amazon.com/bin/view/AWS_Security_Sauron_V3) APIs and provides a a convenience wrapper around the [AWSSECSauronServicePythonClient](https://code.amazon.com/packages/AWSSECSauronServicePythonClient/) auto-generated Coral Python client (not very user-friendly). This package is also available within the [AutomatedRunbooks](https://w.amazon.com/bin/view/AWS_IT_Security/SecDevOps/AutomatedRunbooks) service.The new APIs are specific to Watchlist email reports and expose the following functionality:  

1.  create_watchlist_email_report
2.  get_watchlist_email_report
3.  search_watchlist_email_reports (MongoDB query syntax)
4.  text_search_watchlist_email_reports (regex query syntax)


CRs: 

Add P1 APIs create/get/search watchlistemailreport to SauronPythonClient - sim:SECDEVOPS-5090

https://code.amazon.com/reviews/CR-75212233/revisions/2#/details

There are the get, create, search, and textsearch APIs for both the issues reports and watchlist email reports

The documentation is built-in
When using AR you can type `?` after anything and it will show you good built-in help

Full code is here: [https://code.amazon.com/packages/SauronPythonClient](https://code.amazon.com/packages/SauronPythonClient)


File with all APIs defined is this one: [https://code.amazon.com/packages/SauronPythonClient/blobs/mainline/--/src/sauron_client/sauron_api_client.py](https://code.amazon.com/packages/SauronPythonClient/blobs/mainline/--/src/sauron_client/sauron_api_client.py)

---

But on the CR link I sent, click the `File diff` tab

I actually have one more question: I want to gain access to full features of Sauron including on-call activities etc. who I can reach out to submit the request do you know? right now I only have access to action items, issues, watchlist sections.

![white_check_mark](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F2705%402x.png)![eyes](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F1f440%402x.png)![raised_hands](https://slack-imgs.com/?c=1&o1=gu&url=https%3A%2F%2Fa.slack-edge.com%2Fproduction-standard-emoji-assets%2F13.0%2Fapple-small%2F1f64c%402x.png)

![](https://ca.slack-edge.com/E015GUGD2V6-W01875PK6DN-4cdcc7afbdf6-48)

[Todd Leonhardt](https://app.slack.com/team/W01875PK6DN)  [6:36 PM](https://amzn-aws.slack.com/archives/D03T95LFP47/p1662071805509149)  

That is part of the Team Configuration on a per-team basis.  So if you want access to the Cloud Response stuff, you need to reach out to a CloudSec site lead or manager.