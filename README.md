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

// Review videos one more time 

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

