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
