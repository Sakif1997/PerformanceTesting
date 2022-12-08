
# Performance Testing Report

A brief description of what this project does and who it's for


## Installation



Java
https://www.oracle.com/java/technologies/downloads/

JMeter
https://jmeter.apache.org/download_jmeter.cgi

Click =>Binaries
=>apache-jmeter-5.5.zip

We use BlazeMeter to generate JMX files
https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi?hl=en
    
## Test Plan
Testplan > Add > Threads (Users) > Thread Group (this might vary dependent on the jMeter version you are using)

Name: Users

Number of Threads (users): 1 to 6

Ramp-Up Period (in seconds): 10

Loop Count: 1

The general setting for the tests execution, such as whether Thread Groups will run simultaneously or sequentially, is specified in the item called Test Plan.

All HTTP Requests will use some default settings from the HTTP Request, such as the Server IP, Port Number, and Content-Encoding.

Each Thread Group specifies how the HTTP Requests should be carried out. To determine how many concurrent "users" will be simulated, one must first know the number of threads. The number of actions each "user" will perform is determined by the loop count.

The HTTP Header Manager, which allows you to provide the Request Headers that will be utilized by the upcoming HTTP Requests, is the first item in Thread Groups.




## List of API

https://www.opencart.com/index.php?route=common/home
https://www.opencart.com/index.php?route=cms/feature
https://www.opencart.com/index.php?route=marketplace/extension
https://www.opencart.com/index.php?route=cms/company
https://www.opencart.com/index.php?route=account/login
## API Deployment

#### Run BlazeMeter

#### Collect Frequently used API

#### Save JMX file then paste => apache-jmeter-5.5\bin




## Deployment Process
Load the JMeter Script

File > Open (CTRL + O)
Locate the "OPENCART_T1.jmx" file contained on this repo
Continue open OPENCART_T1 to OPENCART_T6
Open those file
The Test Plan will be loaded
![p11](https://user-images.githubusercontent.com/45315685/206380318-ef01e209-0216-41f4-81f9-a85a215d1f40.jpg)

