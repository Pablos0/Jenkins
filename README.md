# Jenkins

## Preparing environment for CI

Open the browser with the next path http://localhost:8080/login?from=%2F <br><br>
In case the 8080 is taken, you may stop service and go the file `jenkins.xml` file. Look for -Xrs -Xmx256m line (41) and change the port.

Missing plugIn 
SSH slaves, Windows Slaves, Pipepline build

<strong>Creating first Jenkins work</strong><br>

Username Pablos

Create a new job
- Build an step
`ECHO Hello!`
- Click play button 
- Cick in # icon
- Go to console Output

### Build triggers
1. On-demand run
2. Other job finish
3. Cron schedule
4. SCM check

<strong>Preparing trigger</strong>

- Select the job
- Go to settings
- Look for Triggers option
- Build after other prohects are built
- Go back to the main page and schedule the build

### Cron syntax

- Select the job
- Go to settings
- Look for Triggers option
- Build periodically
- In the question mark you may see the syntax

<strong>Poll SCM - Will be run after each commit</strong>

### Git integration

1. Install Git plugin
2. Let Jenkins know where Git is installed (%GIT_HOME%\cmd\git.exe)

In the job configuration look for Source Management and select Git. You must specify the address of the repository. *Validate if the main branch of the repository is MAIN or MASTER*
After that go to  Global Tool Configuration and check if the display path for Git in Jenkins is the same that the computer. Add name you may the version of Git.

### Maven integration

Go to Global Tool Configuration and look for Maven, select Add Maven fill the fields just as Git. In name type the version of Maven and path type the location of maven in your conputer.
You may go to configuration of a job a look for Build, select *Invoke top-level Maven targets* option.In Goals field, type the reason of the build. Select advance and in POM field type the path of the POM file from the project. 

### Artifacts

When you create  a job in Build type the command  ECHO hello > file_name.txt. Once you run the build a file with be create with the information typed. Go to Add post-build Actions and select Archive the Artifacts, the run the build one more time. If the job is successfully a permanent link will be created. 

You may copy the created files in another job. In the build configuration select *Copy artifacts from another project* option and type the name of the project along the file name to be copied. 

### Nodes 

Nodes may be as a tool when you have several jobs to be run. Sometimes have just one node won't be enough. 

To run a job in certain Node you must go to configure job and select <strong>Restrict where this project can be run </strong>, the select the label to be use. 

### Nodes on Linux

1. Create node on master
2. Connect linux slave and install OpenJDK
3. Wget <strong>agent.jar</strong> from master node
4. Run slave from command line

To create a node you may access to https://www.jenkins.io/doc/book/using/using-agents/#set-up-agent1-on-jenkins 

### Uninstall Jenkins

1. Run the CMD as administrator
2. run the coman *sc delete jenkins*
3. Go the directory where Jenkins is located and delete it 

### Extra information

chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://elearn.epam.com/assets/courseware/v1/371657f06ea01ef59a450e60cbd20095/asset-v1:EPAM+CIJ+ENG+type@asset+block/DevTestOps-CI_with_Jenkins.pdf

https://www.jenkins.io/

