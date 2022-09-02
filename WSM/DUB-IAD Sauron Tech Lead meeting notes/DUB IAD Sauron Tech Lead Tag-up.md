---
created: 2022-09-01T12:29:10-04:00
updated: 2022-09-01T13:08:33-04:00
---
what is PR/FAQ
https://w.amazon.com/bin/view/WorkingBackwards/PRFAQ

**Getting Started:** 

-   Before writing the PR/FAQ, understand how it fits into the [Working Backwards Process](https://w.amazon.com/bin/view/WorkingBackwards/Process) and the [5 Customer Questions](https://w.amazon.com/bin/view/WorkingBackwards/5CustomerQuestions/#H2.28Define29Whatistheprevailingcustomerproblem2Fopportunity3FWhatdatainformedthis3F).
-   If you are not yet ready to write a full PR/FAQ, try starting with a [mini PR/FAQ](https://quip-amazon.com/IZrsASnIqgBe/Mini-PRFAQ-Template) to get your ideas down. 
-   Use the [PR/FAQ Writing Tool](https://console.harmony.a2z.com/pr-faq-writing-tool/) to draft a downloadable document with step-by-step tips and examples.
-   Download the [Working Backwards Document Guide](https://amazon.awsapps.com/workdocs/index.html#/document/b8958f5c58208bed71c26dc3f97377e7c668830f35b548202eec81e54942b1a8). The guide includes instructions, tips, guidance, and editing checklists.
-   Visit the sub-pages on this wiki for guidance on Press Releases, FAQs, and Visuals.
-   For AWS-specific guidance, [visit this wiki](https://w.amazon.com/bin/view/AWS/WorkingBackwards/). If you need to write a wire-ready PR/FAQ going up to senior AWS leadership, take the [on-demand wire-ready PR training](https://knet.amazon.com/?%252fDeepLink%252fProcessRedirect.aspx%253fmodule%253dlodetails%2526lo%253d30726608-4c15-4971-af6f-d694c43deee3).
-   For tips on coaching and reviewing PR/FAQs as a leader, [visit this wiki.](https://w.amazon.com/bin/view/WorkingBackwards/PRFAQ/Coaching_Reviewing_PRFAQs/)


Create FR request in sim ticket system - use below link
https://sim.amazon.com/issues/create?template=99766720-3a30-4610-a4ec-bbcecf88ebf3

[SV3] - Request root cause and involved services fields in Characteristics section to be editable instead of dropdown list
https://sim.amazon.com/issues/SECDEVOPS-5147

# Large scale operations
https://w.amazon.com/bin/view/AWS_Security_Sauron_V3/Design_Decisions/Large_scale_operations

https://sim.amazon.com/issues/SECDEVOPS-5065

pending tasks:

submit feature request: (use sim ticket system to cut the ticket)
I am looking into Characteristics section of each Sauron. Root cause and involved services two fields are important to us. we want to manually enter the root cause after discussing with service team, also manually enter the services who own the WSM write ups. right now having them as drop down does not make sense, our team can manually enter this info and make it meaningful for reporting. let me know if this is something your team can make a coding change? if this is possible, I would want it prioritized because the information is crucial for us,  right now I believe no one is entering these 2 fields, but our team can enter the info.  am not sure if we capture this info in DW or not, but it needs. to be in DW as well.

Will will take this: 
currently there is no relations between Sauron's and sim data , since sim ticket has multiple alias , and 1 Sauron can have multiple sim sim/tt attached, I would want a table to be created to bridge this gap, for each Sauron , what are the unique sim tickets linked , so that I can easily pull sim ticket info as needed


A better approach would be to merge Sauron and tpm helper , at least for the data sets , let Sauron deal with Sauron data , tpm helper deal with tickets , different set of tables .