# Performance_Testing

## Introduction: 
Pioneer Alpha website has been taken for performance testing in JMeter.

## Elements for a complete JMeter flow:
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
   - Select the pioneer alpha.com
   - Then paste => **apache-jmeter-5.5\bin**
   - File > Open (CTRL + O)
   - Locate the "Pio.jmx" file contained on this repo
   - Continue open Pio
   - Open those file
   - The Test Plan will be loaded     
   ![c](https://github.com/Anika154/Performance_Testing/assets/54212195/9b666c91-39ac-4dda-8ef9-0675238140ed)
### Make jtl file

```bash
  jmeter -n -t  Pio_report.jmx -l Pio_report.jtl
```      
Then continue to upgrade Threads(1 to 10) by keeping Ramp-up the same.
  
  ![a](https://github.com/Anika154/Performance_Testing/assets/54212195/1fddbed0-1040-4637-b831-94b7f7025077)
 
  
  ![d](https://github.com/Anika154/Performance_Testing/assets/54212195/efed3e1d-ce7d-4c09-a1d4-a5bc159a17ba)

After completing this command
   ### Make html file   
  
  ```bash
  jmeter -g report\Pio_report.jtl -o report\Pio_report.html
```

  ![b](https://github.com/Anika154/Performance_Testing/assets/54212195/d99e8618-b9e8-48fb-88ae-fc49d03c39d4)  
  ![f](https://github.com/Anika154/Performance_Testing/assets/54212195/89dca3ab-f23c-4e27-ad56-591144a24ec4)

# HTML Report

**Number of Threads 10 ; Ramp-Up Period 10s**
   
Requests Summary             |  Errors
:-------------------------:|:-------------------------:
![1](https://github.com/Anika154/Performance_Testing/assets/54212195/4df13c71-83e3-4495-97ee-7ca423cf14ea)  |  ![2](https://github.com/Anika154/Performance_Testing/assets/54212195/11c51bb7-5634-440e-920a-5616a0c62a26.jpg)


**Application Performance Index**             

![b](https://github.com/Anika154/Performance_Testing/assets/54212195/86db3b03-d33a-4c4c-9409-903642079709)



