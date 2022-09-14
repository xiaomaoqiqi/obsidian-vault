---
created: 2022-09-11T22:08:46-04:00
updated: 2022-09-11T22:10:48-04:00
---

How to solve: # The security token included in the request is expired

```
ada credentials setup
```

```
kinit -f && mwinit -o
rm ~/.aws/credentials
ada credentials update --account=254241016566 --provider=conduit --role=IibsAdminAccess-DO-NOT-DELETE --profile=default --once
```

according to this wiki: [https://w.amazon.com/bin/view/PrimeTeam/MCX/YVR/Setup_and_How_To/HowToUseAda/#HSettingupaProfilewithAda](https://w.amazon.com/bin/view/PrimeTeam/MCX/YVR/Setup_and_How_To/HowToUseAda/#HSettingupaProfilewithAda)

