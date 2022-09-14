---
created: 2022-09-06T11:57:40-04:00
updated: 2022-09-08T23:18:10-04:00
---

https://w.amazon.com/bin/view/AWS_IT_Security/Operations/CSE/Training/Zero_to_Hero_NAWS_Training/


We can use NAWS for the endpoint

The implementation is similar to [https://prod.findmysecops.security.aws.dev/](https://prod.findmysecops.security.aws.dev/)


That is 100% NAWS and is from that guide

A good POC could be James but also [@donahup](https://amazon.enterprise.slack.com/team/W0154LV2HN3) (creator of the above endpoint and ex SecOps engineer)




Xiaoqipm devdesktop 
https://builderhub.corp.amazon.com/app.html#/cloud-desktop/users/xiaoqipm

Start using it right away:

-   [SSH in browser](https://ssh.corp.amazon.com/?tabs=dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com "https://ssh.corp.amazon.com/?tabs=dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com")
-   Connect in a terminal: 
    
    ssh dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com





**The [Brazil Build System](https://w.amazon.com/bin/view/BrazilBuildSystem "BrazilBuildSystem"), Amazon's internal software development and release management toolchain.**


**Tool: bones**

Description: The BONES CLI is a walkthrough of getting started with Builder Tools and Native AWS. It will assist you in getting a brand new pipeline deploying to your own AWS account, either by creating a new service from scratch or by migrating an existing application.

Team: nade-team

Email: nade-team

  

For more information about this tool, see https://builderhub.corp.amazon.com/docs/bones-cli.html

To report bug/issue, see http://tiny.amazon.com/3dg4ktoe



Tool: brazil-octane

Description: Octane CLI

Team: builderhub-team

Email: builderhub-team@amazon.com
For more information about this tool, see https://w.amazon.com/index.php/Octane_CLI


Tool: ada

Description: Aws Developer Account

Team: Rapid Dev Cycle Team

Email: rdct-team@amazon.com
For more information about this tool, see https://w.amazon.com/bin/view/DevAccount/Docs/


Tool: brazilcli

Description: Brazil CLI

Team: Build Execution

Email: bx-team@amazon.com
For more information about this tool, see https://w.amazon.com/index.php/BrazilCLI_2.0


Tool: hub-create
Description: BuilderHub Create account onboarding tool
Team: hub-team
Email: hub-team@amazon.com

For more information about this tool, see https://code.amazon.com/packages/BuilderHubCreateOnboarding/blobs/mainline/--/README.md


Bindle
xiaoqipm's PersonalSoftwareBindle (PersonalSoftwareBindle)

New AWS Isengard account for NAWS training

## AWS Account

Email

xiaoqipm+xiaoqinawstraining-app@amazon.com

Account Name

xiaoqinawstraining-app

Secondary Owner

adnanjam

Financial Owner

adnanjam

Posix Group Owner

aws-security-straws-posix


Builder Hub
https://create.hub.amazon.dev/cloned-applications/XiaoqiNAWSTraining

tldr - Bindle locks are a mechanism to verify whether an individual or group can perform an action or set of action(s) based on predefined permissions, through Bindles. In other words, it's a way for us to manage authorization & permissions. BRASS is an authorization service we can leverage via their API to check whether an actor should have access to a particular set of resources (managed by bindles). 

Finally, "why do we need these?". Well for starters, we need a way to gate access to our API / backend lambdas. We are going to restrict access to our UI via CloudFrontSigner. But this is not solely enough. Therefore, we need a way to handle authorization on our API's.

CloudFrontSigner is an Amazon service which enables service owners to gate their CloudFront distributions with Midway and Bindles. Midway is used for _authentication_ and Bindles is used for authorization. After onboarding a domain, a Bindles resource is created where service owners can grant access to only certain users or groups.


TL;DR: LDAP is a protocol, and Active Directory is a server. LDAP authenticates Active Directory – it’s a set of guidelines to send and receive information (like usernames and passwords) to Active Directory.


**BATS (Build Artifact Transform Service)** is a packaging service; it takes build artifacts (e.g. from Brazil), transforms them in some way (e.g. into a Lambda deployment package), and publishes the result in some fashion (e.g. to S3 or ECR). BATS is used in native AWS deployments through Pipelines, and packaging for the Hydra Test Platform.


## NICE DCV

https://builderhub.corp.amazon.com/docs/dev-setup/clouddesktop-optional-gui-dcv.html

copy file from cloud desktop to local machine

```
scp xiaoqipm@dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com:/usr/share/dcv/cdd/dcv-cdd.py /Users/xiaoqipm/Documents/DCV
chmod +x /Users/xiaoqipm/Documents/DCV/dcv-cdd.py
```

install dcv-cdd.py connection script

```
python3 /Users/xiaoqipm/Documents/DCV/dcv-cdd.py connect dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com

```
dcv list-sessions
```
python3 /Users/xiaoqipm/Documents/DCV/dcv-cdd.py close-session dev-dsk-xiaoqipm-1e-e925b816.us-east-1.amazon.com



```

Burner account creation 

https://conduit.security.a2z.com/burner-accounts


### [Set up your Brazil workplace]

A Brazil workplace is a directory used to hold your workspaces. A workspace contains the package(s) that you’re working on and their dependencies. On Cloud Desktops, your Brazil workplace is expected to be at the location /workplace/${USER}. Create and claim ownership of this directory now:

```
sudo mkdir -p -m 755 /workplace/${xiaoqipm}
sudo chown -R ${xiaoqipm}:amazon /workplace/${xiaoqipm}
```

If you want to simply refer to this location as ~/workplace (_recommended_, for consistency with other platforms, such as your laptop), make a link to it from your home directory:

```
ln -s /workplace/${xiaoqipm} ~/workplace
```


Run `ln -s /Volumes/workplace ~/workplace` to generate a symlink that makes it look like the workplace folder is in your home directory.


ls -lra -> show accounts and owners


-rw-r--r-- 12 linuxize users 12.0K Apr  28 10:10 file_name
|[-][-][-]-   [------] [---]
| |  |  | |      |       |
| |  |  | |      |       +-----------> 7. Group
| |  |  | |      +-------------------> 6. Owner
| |  |  | +--------------------------> 5. Alternate Access Method
| |  |  +----------------------------> 4. Others Permissions
| |  +-------------------------------> 3. Group Permissions
| +----------------------------------> 2. Owner Permissions
+------------------------------------> 1. File Type



Change ownership 
sudo chown xiaoqipm /workplace

dev-dsk-xiaoqipm-1e-e925b816 % ls -lra
total 8
dr-xr-xr-x 20 root     root   4096 Sep  7 15:42 ..
drwxr-xr-x  2 xiaoqipm amazon 4096 Sep  7 15:42 .


SDF -> # Service Description File


 NAPS - [Named AWS Policies Site (Managed Policies Tool)](https://naps.amazon.com/)



make code changes 

https://builderhub.corp.amazon.com/docs/bt101-make-code-change.html

Let’s look at the details of our workspace. We could run brazil workspace show, but the sub-command **workspace** can be shortened to **ws** for any commands that manipulate your workspace

A [version set] is a data structure that contains all of a package’s dependencies and their versions. A version set lets you precisely manage the packages your software project depends on. You can add new packages, update existing packages, and remove packages from a version set as your software’s dependencies change over time.


dev-dsk-xiaoqipm-1e-e925b816 % bws show
Workspace:              xiaoqipm_workspace
    Root:               /workplace/workspace
    Version Set:        BT101Xiaoqipm/development@6094692650
    Platform Override:  AL2_x86_64
    Packages:
                        BT101Xiaoqipm-1.0 -> .
                        BT101XiaoqipmTests-1.0 -> .




A [package] is the smallest buildable/deployable unit. Packages are structured as code with similar functionality that should be built and deployed together, and is often a library that performs some function or an application that is actually run. External dependencies are declared in the package’s Config file, often called the “big C” or “capital C” config file because it is always capitalized.



For this training, we will be using a CLI based text editor. **vim**, **emacs**, and **nano** are already installed on your Cloud Desktop, and you can use whichever you prefer (if your Cloud Desktop is _Amazon Linux 2_, **nano** is not installed by default. To install it, run sudo yum install nano).

If you have no previous experience with a CLI based text editor, we recommend that you use **nano**. All steps will assume you are using **nano** and provide the necessary commands.

If you plan to use **nano**, we recommend that you run the two commands below. They will add syntax highlighting to make the code more readable, and replace tabs with spaces to prevent build errors. Run the following commands on your Cloud Desktop:

```
ls -1 /usr/share/nano/java.nanorc | sed 's/^\//include \//' >> ~/.nanorc
echo "set tabstospaces" >> ~/.nanorc
```



1.  To see if your packages build successfully, first go to your package root directory (unless you’re already there):
    
    ```
    cd ~/workplace/BT101/src/BT101Username
    ```
    
2.  Make sure the package will build by using **brazil-build**:
    
    ```
    brazil-build
    ```
    
    Important
    
    _If your build fails_, your pipeline may not have finished building the version set. Open up the browser window where you had your pipeline open, or go to [https://pipelines.amazon.com](https://pipelines.amazon.com/)  and open your BT101 pipeline, and make sure that the status of the VersionSet stage is Succeeded. If it is not, wait for it to finish and then re-run the brazil workspace sync command in the previous step before building. If your build has failed and you verified that your pipeline finished building the version set, you may have an issue with CheckStyle.
    
    _CheckStyle_ is a source code analyzer used by many teams at Amazon to ensure that code adheres to a coding standard. Standards are set at the team level and any code that does not meet that standard will fail to build.
    
    Check the build failure output, and look for the word CheckStyle. If you find it, the issue you are facing is likely due to a copy/paste action inserting a tab instead of spaces. Also find the line number referenced in the build failure. If you are using **nano**, you can jump to a specific line by pressing Ctrl+_ and entering the line number. Use your arrow keys to find any tab characters, and _replace them with spaces_ before running your build command again.



1.  Make sure the package will still build, and this time we will run the unit tests as well. The brazil-build release command will build your package, run all unit tests, and perform style checks. You can run **brazil-build** just to build your package, brazil-build test to build and test your package, but for now we want to run everything. Before running the **brazil-build** command, make sure you are in the root folder of the correct package:
    
    ```
    cd ~/workplace/BT101/src/BT101Username
    
    brazil-build release
    ```


### Stage and commit your changes

We have made changes to our service and enabled the appropriate unit tests locally, now let’s make the changes available for others to review before we release them.

1.  To see what files you’ve changed before staging, run:
    
    ```
    git status
    ```
    
    It should show the two files that you modified:
    
    ```
    On branch mainline
    Changes not staged for commit:
       (use "git add <file>..." to update what will be committed)
       (use "git checkout -- <file>..." to discard changes in working directory)
    
       modified:   src/com/amazon/bt101username/lambda/calculator/Calculator.java
       modified:   tst/com/amazon/bt101username/lambda/calculator/CalculatorTest.java
    ```
    
    Note
    
    Most teams will check out and develop against a branch rather than developing directly on the mainline. Be sure to learn the best practices followed by your team.
    
2.  Stage your changes by running:
    
    ```
    git add src tst
    ```
    
    This command tells git that you want to include changes to the src and tst directories in the next commit. If you want, run git status again to verify that the two files are now staged. Instead of “Changes not staged for commit” you’ll see “Changes to be committed”, and the filenames will be shown in green instead of red.
    
3.  Commit your changes by running:
    
    ```
    git commit -m "Implement subtract function and enable subtract unit tests"
    ```
    
    Important
    
    _Don’t push your changes yet!_ First, you’ll create a code review (CR) using the commit you just made.


OnBoardBrass

{ "Version": "2012-10-17", "Statement": [  
{ "Effect": "Allow",  
"Action": [ "BrassService:OnboardCaller" ],  
"Resource": "*" } ] }

To be able to call BRASS via AWS Auth, you must set up the proper inline IAM policies for your IAM user or role. Set the action(s) to the appropriate APIs that you need in the format of "BrassService:Operation". Operation here is the same as the API name. For example:

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "<INSERT ID HERE>",
            "Effect": "Allow",
            "Action": [
                "BrassService:IsAuthorized"
            ],
            "Resource": "*"
        }
    ]
}

If you're using the IAM console, you may see an error saying it does not recognize BrassService. That's ok, grant the permission anyway.

You will need to add **ALL** API that you are going to call BRASS. In addition, BrassService does not provide specific resources for service actions, so the wildcard asterisk is used.


Brass is a service for determining group membership. So, zero to hero, and many of the applications across amazon will use Brass to verify whether an authenticated (authn) user is authorized (authz). To onboard to Brass, we have to use their tool. Their tool is deployed via Apollo, hence why we have to use Apollo. Otherwise, we wouldn't use Apollo at all. You have Apollo on your dev desk, so you shouldn't need it on your local machine. You simply need to run a command once to onboard and you will never run it again. 



Now onboard to BRASS with the following commands (FYSA -  We have to onboard to a particular region and BRASS is not yet exposed in all regions so choose carefully. More about that here: [https://w.amazon.com/bin/view/BRASS/Onboarding/AWSAuth/#HAWSAuthEndpoints](https://w.amazon.com/bin/view/BRASS/Onboarding/AWSAuth/#HAWSAuthEndpoints))]



/apollo/bin/env -e BrassOpsTools /apollo/env/BrassOpsTools/bin/brass_awsauth -e prod-pdx -r us-west-2 onboard-caller GROUP


{
  "onboarding": {
    "onboardedCaller": {
      "callerType": "AWS_ACCOUNT",
      "callerId": "859900930677"
    },
    "onboardedTarget": {
      "targetType": "GROUP"
    },
    "onboardedBy": "AwsAccount:859900930677",
    "createdAt": 1662666392.109
  },
  "__type": "com.amazon.brass.coral.calls#OnboardCallerResponse"
}





_This command [onboards our AWS account](https://w.amazon.com/bin/view/BRASS/Onboarding/GuideForSelfServiceOnboarding/#HUsingtheBRASSCLI-4) and allows to us to request group membership from any resource using [this policy](https://code.amazon.com/packages/BrycesecNAWSTrainingCDK/blobs/0df3b2e13eab7d07649324fad0c0e1338365b38d/--/lib/stacks/backend.ts#L72-L79)._


lambda.addToRolePolicy(

new PolicyStatement({

sid: "AllowBRASSAccess",

effect: Effect.ALLOW,

actions: ["BrassService:IsAuthorized", "BrassService:IsMemberOf"],

resources: ["*"],

})

);

return lambda;


/apollo/bin/env -e BrassOpsTools /apollo/env/BrassOpsTools/bin/brass_awsauth -e prod-pdx -r us-west-2 onboard-caller BINDLE_LOCK



# BrycesecNAWSTrainingCDK
https://code.amazon.com/packages/BrycesecNAWSTrainingCDK/blobs/0df3b2e13eab7d07649324fad0c0e1338365b38d/--/lib/stacks/backend.ts#L72-L79


{
  "onboarding": {
    "onboardedCaller": {
      "callerType": "AWS_ACCOUNT",
      "callerId": "859900930677"
    },
    "onboardedTarget": {
      "targetType": "BINDLE_LOCK"
    },
    "onboardedBy": "AwsAccount:859900930677",
    "createdAt": 1662667150.112
  },
  "__type": "com.amazon.brass.coral.calls#OnboardCallerResponse"
}



4.  Now that we are onboarded, lets run a check to see if our alias can unlock our bindle, which it should! (Make sure with the below command to provide your Bindle Lock ID, not your Software App Bindle ID. *Replace brycesec with your username and "amzn1.bindle.resource.xadsafdwefwfwef" with your bindle lock found on the top of the bindle lock page.

/apollo/bin/env -e BrassOpsTools /apollo/env/BrassOpsTools/bin/brass_awsauth -e prod-pdx -r us-west-2 is-authorized --actor.actor-type principal --actor.actor-id xiaoqipm Unlock Bindle Lock amzn1.bindle.resource.lqtkr5qwy6soi74w4vsa

Note: 
after running above commands, if it pops error saying security token is expired, repeat below steps again: 
1.  go here: [https://isengard.amazon.com/console-access](https://isengard.amazon.com/console-access) , search for your alias, and select the double-box icon to the right of the a Admin role for the Isengard account you created 
 
2.  select "bash/zsh" and copy the text there

3.  paste these commands into your dev desktop


4.  type "aws sts get-caller-identity" to confirm that your Role credentials are valid for the right account.




Additional Notes: 
# What's BONES?

The BONES CLI enables you to create a complete Native AWS service by answering a few questions. It does the work of creating all of the resources you need and ties it together with a pipeline.

TL;DR
https://w.amazon.com/bin/view/NAWSForDummies/Fundamentals/BONES/


Sample CDK Pkg 
https://code.amazon.com/packages/BrycesecNAWSTrainingCDK/trees/mainline


So the zerotohero wiki shows how to clone a package: [https://w.amazon.com/bin/view/AWS_IT_Security/Operations/CSE/Training/Zero_to_Hero_NAWS_Training/#HFrontend28UI29package](https://w.amazon.com/bin/view/AWS_IT_Security/Operations/CSE/Training/Zero_to_Hero_NAWS_Training/#HFrontend28UI29package) <--- step 7 Brazil CLI docs are here: [https://builderhub.corp.amazon.com/docs/brazil/cli-guide/reference.html](https://builderhub.corp.amazon.com/docs/brazil/cli-guide/reference.html)you can also use brazil -h for help



git clone ssh://git.amazon.com/pkg/InstallUnisonAL2  
cd InstallUnisonAL2  
./install-unison $2.52.1 $4.14.0



																																											
ESLint is a static code analysis tool for identifying problematic patterns found in JavaScript code. It was created by Nicholas C. Zakas in 2013. Rules in ESLint are configurable, and customized rules can be defined and loaded. ESLint covers both code quality and coding style issues


																																																									

																																																				


																																									

																																									