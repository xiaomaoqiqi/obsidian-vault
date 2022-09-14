---
created: 2022-09-08T17:37:29-04:00
updated: 2022-09-11T23:06:34-04:00
---


In order to start a new project on local , run the following commands:

1.  `brazil ws create --name XiaoqiNAWS`
2.  `cd XiaoqiNAWS`
3. `brazil ws use -p XiaoqiNAWSTrainingCDK`
4. `cd src/XiaoqiNAWSTrainingCDK`
5.  `brazil-build`


Note: you need to go to https://create.hub.amazon.dev/cloned-applications/XiaoqiNAWSTraining, then copy the version set while cloning the package from CDK to your mac
workspace name should be the same as your CDK package name

YourPackageName could be the CDK package you are trying to get onto local.

If you want to get new dependencies you added to your version set onto your local you can run:

1.  `brazil ws --sync --md`

then you can use VsCode to open Brazil pkg from local machine. 

There are several ways, many of which are documented here: [https://builderhub.corp.amazon.com/docs/dev-setup/clouddesktop-optional-laptop-sync.html](https://builderhub.corp.amazon.com/docs/dev-setup/clouddesktop-optional-laptop-sync.html)


# CDKBuild-2.x does not exist in the version set when calling brazil-build release


Resolution:  
brazil ws merge --package CDKBuild-2.x

from cloud desktop, to sync code from git to local, run: 
brazil ws sync 
git pull 

Run the unit tests with:

```
brazil-build test
```






