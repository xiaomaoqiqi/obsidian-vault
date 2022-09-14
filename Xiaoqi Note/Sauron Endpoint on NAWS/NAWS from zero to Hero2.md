---
created: 2022-09-08T23:18:57-04:00
updated: 2022-09-11T17:18:26-04:00
---

## The `brazil-build` command is too long!

It is recommended that you set up an alias like this in your `.zshrc` (or other shell init):

  
 alias bb=brazil-build  

If you want to set up an alias on Mac, you can add the previous line into .bash_profile file (or other shell init) and refresh the file:

  
 source ~/.bash_profile  

And you need to close old shell window/tab to make the new added alias work.

```
alias bb="brazil-build"
alias bba='brazil-build apollo-pkg'
alias bre='brazil-runtime-exec'
alias brc='brazil-recursive-cmd'
alias bws='brazil ws'
alias bwsuse='bws use --gitMode -p'
alias bwscreate='bws create -n'
alias brc=brazil-recursive-cmd
alias bbr='brc brazil-build'
alias bball='brc --allPackages'
alias bbb='brc --allPackages brazil-build'
alias bbra='bbr apollo-pkg'
```


1.  toolbox install mechanic
2.  Verify installation: mechanic --help
3.  Verify access: mechanic get user
4.  Optional: Setup Autocomplete:mechanic configure completion
    1.  See error compdef not found? Run:

autoload -Uz compinit

compinit


how to solve ERROR: You have no preference setting for Node 12.x

 after `brew install node@14`, I had to manually run `echo 'export PATH="/opt/homebrew/opt/node@14/bin:$PATH"' >> /Users/xiaoqipm/.bash_profile` and `source /Users/xiaoqipm/.bash_profile`In the end, run `which node` to get the node path used to copy and paste into question prompted by the command `brazil setup --node`
note: /opt/homebrew/opt/node@14/bin/node

You also might need to change the config on the cdk and frontend packages to use node 14 as 12 is now EOL

NodeJS documentation 

https://w.amazon.com/index.php/BrazilCLI%202.0/Runtimes/NodeJS


How to solve issue: CDKBuild-2.x/runtime.dep does not exist

Method: brazil ws merge --package CDKBuild-2.x

if facing below error: **Can't find some of the packages in the source version set.**

**BMDS exception thrown while calling preview merge: The following explicitly requested major versions do not exist in the version set 'live'**

run ```
brazil ws merge clean then brazil ws merge --package CDKBuild-2.x

** How to solve Error: You have no preference setting for Java 8

## Install Amazon Corretto 8

1.  Download the Mac `.pkg` file 
    
2.  Double click the downloaded file to start the installation wizard. Follow the steps in the wizard.
    
3.  Once the wizard completes, Amazon Corretto 8 will be installed in `/Library/Java/JavaVirtualMachines/`.
    
    You can run the following command in a terminal to get the complete installation path.
    
    `/usr/libexec/java_home --verbose`
    
4.  Optionally, run the following commands in the terminal to set the `JAVA_HOME` variable.
    
    `export JAVA_HOME=/Library/Java/JavaVirtualMachines/amazon-corretto-8.jdk/Contents/Home`

then  run the command **brazil-recursive-cmd --allPackages brazil-build** on terminal at your workspace location.



# difference between brazil-build VS brazil-recursive-cmd brazil-build


You can have multiple packages in your local workspace.

-   `bb` aka `brazil-build` runs the brazil build system in the package you're currently in.
-   `brazil-recursive-cmd` looks at the package you're in, find all of its dependencies that are also checked out in your local workspace, and then recursively invokes `brazil-recursive-cmd [your command]` in those dependent packages. Then, it runs the command in your current package.

So for example, if you have 2 packages in your workspace, one named `Library` and one named `Service` and `Service` depends on `Library`, then:

-   `~\workspace\Service$ brazil-build` will run the brazil build system in `Service`, and it will not run it in `Library`.
-   `~\workspace\Service$ brazil-recursive-cmd brazil-build` will run the brazil build system in `Library` and then it will run the brazil build system in `Service`.


**_brazil-build_** focuses on building a package by only building the local package (which, if none of the overridden dependent packages have changed, is faster).

If you want brazil to build all of the local packages in the dependency tree, you must invoke **_brazil-recursive-cmd brazil-build_**.



#  fix package-lock.json lockfileVersion so npm uses a specific format?


npm WARN read-shrinkwrap This version of npm is compatible with lockfileVersion@1, but package-lock.json was generated for lockfileVersion@2. I'll try to do my best with it!

to overcome this issue, running the command

```javascript
npm i -g npm@latest
```

globally and running the command

```javascript
npm i npm@latest
```

in the project file helped me resolve the issue.


how to install eslint 

```javascript
sudo npm install -g eslint
```


fix format issue: 

Try running 
bre npm run format 
from within your brazil workspace. You may have to manually fix style issues in lib/app.ts.


Important Notes: 
1.  Finally, make sure to configure your CDK package (specifically to your pipeline) to auto build / enable changeset approval: [https://code.amazon.com/packages/BrycesecNAWSTrainingCDK/blobs/ac03ab4ad13c5af27457dd5a9e9121742ecfd683/--/lib/app.ts#L50](https://code.amazon.com/packages/BrycesecNAWSTrainingCDK/blobs/ac03ab4ad13c5af27457dd5a9e9121742ecfd683/--/lib/app.ts#L50). Keep in mind if you are building a production application, you should enable CR verification.



Note:
to fixed error related to Nan is not found, try below:
npm install nan then run bb



1.  To run our site locally on our cloud desktop, we can cd in UI package and run: bre npm run start which will stand up a dev server running on port 3000 exposed to CORP. You can browse to this page to view live changes to your UI code, complete with hot freshes!








