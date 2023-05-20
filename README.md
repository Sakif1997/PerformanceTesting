
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

Number of Threads(users): 1 to 6

Ramp-Up Period(in seconds): 10

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

#### Test execution
JMeter should be initialized in non-GUI mode.
Make a report folder in the bin folder.
Run Command in jmeter\bin folder.

### generate csv file
#### Step1. n: non GUI mode
#### Step2. t: test plan to execute
#### Step3. output file with results

go to the folder where the files are and open cmd propt on initialized
#### csv file Comand:  jmeter -n -t  OPENCART_T1.jmx -l OPENCART_T1.csv
#### jtl file comand:  jmeter -n -t  OPENCART_T1.jmx -l OPENCART_T1.jtl
#### html file comand: jmeter -g report\OPENCART_T1.jtl -o OPENCART_T1.html
 
## Generate CSV file in Jmeter

Create a CSV file in the test suite folder and add test data to it.
Add a Config Element CSV Data Set Config in Jmeter.
Configure ' CSV Data Set Config ' based on the need such as providing path of CSV file and variable names and other configs.
Run the test to see if data from the CSV file is read and populated in the results.
Run the test to see if data from CSV file is read and populated in the results.

![af](https://user-images.githubusercontent.com/45315685/206388579-af9b1bcc-503f-43bc-a7b0-36ddc6403c81.PNG)
![jj1](https://user-images.githubusercontent.com/45315685/206388883-e31067fa-b508-4352-92ea-37022e1aaab8.jpg)
![jj2](https://user-images.githubusercontent.com/45315685/206388971-b623c0d8-5fe7-43ba-be70-6479080e331b.jpg)
![jj3](https://user-images.githubusercontent.com/45315685/206389093-05df0ce2-6d30-4df6-b2b8-9c73110877e2.jpg)

## Html reports
Number of threads 1,2,3,4,5
Ramp Up Period: 10s
![ramp1](https://user-images.githubusercontent.com/45315685/206390358-15f57200-4ff2-48c9-9c9a-1c0403641cfc.jpg)
![r2](https://user-images.githubusercontent.com/45315685/206390675-44f138bf-b2be-4e80-a9e7-30853a77974b.jpg)
![r3](https://user-images.githubusercontent.com/45315685/206390726-39224944-f3f3-4c61-aa95-d39b6f69a9cc.jpg)
![r4](https://user-images.githubusercontent.com/45315685/206390789-c47dc56e-42e0-46f2-9f0f-95f1bfd70b70.jpg)
![r5](https://user-images.githubusercontent.com/45315685/206390952-16dbe323-cc92-44ae-a37b-7a84003e1514.jpg)

## Endurance testing
Threads count: 6s  
Initial Delay 0s
Start up Time 10s 
Hold load for 600000milisecond
Shutdown Time 0s
![spike1](https://user-images.githubusercontent.com/45315685/206393247-c1922edd-974e-426a-98c0-02e914dda246.jpg)







