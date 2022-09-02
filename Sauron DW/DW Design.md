---
created: 2022-08-30T13:05:48-04:00
updated: 2022-08-30T13:13:02-04:00
---
Build a separate view to bridge the gap between Sauron and sim tickets, view should contain 
Sauron ID, all sim tickets linked to Sauron (ticket ID, ticket alias), ticket type etc.
Based on the surrogate key from sim tickets table, I should be able to look up detail info related to sim ticket such as resolver group, opened data, status 