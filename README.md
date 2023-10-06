# Performance_Testing
The software testing process used for testing the speed, response time, stability, reliability, scalability, and resource usage of a software application under a particular workload.Performance Testing is checking a software program’s: 
- Speed – Determines whether the application responds quickly
- Scalability – Determines the maximum user load the software application can handle.
- Stability – Determines if the application is stable under varying loads

## Scopes: 
Amar iSchool website has been taken for performance testing in JMeter.

## Process for a complete JMeter flow:
- Test Plan Creation
- Thread Group
- Sampler
- Listener

## Test Plan Creation:
Test Plan is where we add elements required for the JMeter test. It stores all the elements, like ThreadGroup, Timers, etc., and their corresponding settings required to run your desired tests.
## Thread Group:
Thread Group is a collection of Threads/Users. The controls for a thread group allow you to set the number of threads for each group.
- Right click Testplan -> Add -> Threads (Users) -> Thread Group
## Samplers:
The user sends HTTP/HTTPS, FTP, and JDBC requests to an FTP server, a web server, and a database, which is known as a sampler.
- Right click Thread Group -> Add -> Sampler -> HTTP Request
## Listener:
Listener shows the results of the test execution. They can show results in a different format, such as a tree, table, graph or log file.
- Right click Thread Group -> Add -> Listener -> View Result Tree

# Load the JMeter Script 
   - Run BlazeMeter    
   - Save JMX file
   - Select the https://www.amarischool.com
   - Then paste => **apache-jmeter-5.5\bin**
   - File > Open (CTRL + O)
   - Locate the "ISchool.jmx" file contained on this repo
   - Continue open ISchool
   - Open those file
   - The Test Plan will be loaded

   <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/9b666c91-39ac-4dda-8ef9-0675238140ed.jpg" width="59%" />
   
### Make jtl file

```bash
  jmeter -n -t  Amar_iSchool.jmx -l Amar_iSchool.jtl
```      
- Then continue to upgrade Threads(1 to 10) by keeping Ramp-up the same. </br>

<p float="left">
   <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/937ec26d-5107-497e-9b88-a1ce81d6b2e1.jpg" width="39%" hspace="20" /> 
   <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/ea7214cc-56e9-4a9c-bf46-f86d7fba0e0b.jpg" width="26%" /> 
</p>


- After completing this command
### Make html file   
  
  ```bash
  jmeter -g report\Amar_iSchool.jtl -o report\Amar_iSchool.html
```
<p float="left">
   <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/bb9fb9bf-dc2e-457c-b220-84ff504f5603.jpg" width="78%" hspace="20" /> 
   <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/1825a861-f1d7-4974-95d2-4b6182baecca.jpg" width="17%" /> 
</p>   
   



# HTML Report

**Number of Threads 10 ; Ramp-Up Period 10s**
   
Requests Summary             |  Errors
:-------------------------:|:-------------------------:
![1](https://github.com/Anika154/Performance_Testing/assets/54212195/4df13c71-83e3-4495-97ee-7ca423cf14ea)  |  ![2](https://github.com/Anika154/Performance_Testing/assets/54212195/11c51bb7-5634-440e-920a-5616a0c62a26.jpg)

Application Performance Index             |  Statistics
:-------------------------:|:-------------------------:
![1](https://github.com/Anika154/Performance_Testing/assets/54212195/5e9804d0-04c4-46ec-a698-07e1e9526484)  |  ![2](https://github.com/Anika154/Performance_Testing/assets/54212195/028f7baf-122d-4f25-b3b7-a234a160afe3.jpg)


# Read CSV file from JMeter:
API:
- https://www.amarischool.com/contactus
- https://cognito-idp.ap-southeast-1.amazonaws.com/
- https://auth.amarischool.com/emailverification?state=signUp
- https://www.amarischool.com/faq


- Create a CSV file and save it into the bin folder of the JMeter <br/>
<img src="https://github.com/Anika154/Performance_Testing/assets/54212195/d99374e7-f534-431e-a8b5-98830b09d989.jpg" width="59%" />


- Right click on Thread Group -> Add -> Config Element -> CSV Data Set Config in Jmeter <br/>
<img src="https://github.com/Anika154/Performance_Testing/assets/54212195/7967a557-ad0d-42d3-a90a-cc47c7acf34c.jpg" width="59%" />


- Browse File in the CSV Dataset config <br/>
<img src="https://github.com/Anika154/Performance_Testing/assets/54212195/89fe815a-7390-4937-8c93-42581831701a.jpg" width="59%" />

 
- Set the HTTP req by providing IP, parameter according to the CSV variables name <br/>
  
<img src="https://github.com/Anika154/Performance_Testing/assets/54212195/32e821f1-29bd-404c-8f2a-ad005afff490.jpg" width="59%" />


- Add Listener -> Run the test and check the result if data read from CSV file <br/>  


**Number of Threads 10 ; Ramp-Up Period 2s**

<p float="left">
  <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/e3b365ec-bfed-4464-8d5f-9994291bab85.jpg" width="49%" /> 
  <img src="https://github.com/Anika154/Performance_Testing/assets/54212195/f196a0af-48a9-4f06-b9a0-dd9f69bd9774.jpg" width="49%" />     
</p>








