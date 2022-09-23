# Performance test in Apache Jmeter

## What is performance testing?

Is a non-functional testing approach to ensure that the application and the isolated elements of it will perform well under expected workload. 

### The goal is not finding bugs, but to eliminate performance bottlenecks of the app 

The performance testing get the measure of: 

1. Speed
2. Scalability  
3. Stability 

## Types of performance testing: 

1. Load testing 

Simulate user load, anticipate users loads, the objective is identifity bottlenecks 

2. Stress testing 

This involves testing the application under extreme workloads and analyze how it handles the traffic, the objective is identify breaking points   

3. Endurance testing 

It's done to validate if the application can handle the expected load for long periods of time

4. Spike testing

It simulates large spikes in the load generated y the users 

5. Volume testing 

Large number of data is populated in the database and overall software, the objective is testing with bit volume of data and the letting ob database volumes 

## Questions to ask before desing performance script

1. What is our anticipated average number of users (normal load)?

2. What is our anticipated peak number of users?

3. When is a good time to load-test our application (i.e. off-hours or week-ends), bearing in mind that this may very well crash one or more of our servers?

4. Does our application have state? If so, how does our application manage it (cookies, session-rewriting, or some other method)?

5. What is the testing intended to achieve?

## Plugins

1. [Blazemeter](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)

2. [HarJemeter](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)

## Performance testing process

<img width="949" alt="image" src="https://user-images.githubusercontent.com/8729953/190224197-b4c95876-5a9c-4961-9ee2-d207d4f8689d.png">

# Jmeter key notes

1. Thread group: It is the way to simulate users, it's a root element where located the components and functions to be tested 

## State codes HTTP to use assertions

* 404 Bad request
* 200 OK
 
## Correlational dynamic values

1. Sessions IDS
2. Tokes and keys
3. State context of application
3. Others values
  1. Ids
  2. Objects
  3. Dynamics values to test

## Different languages to use Jmeter

Use one depend of the context

1. JavaScript
2. Commons Jexl
3. Groovy (OOP)

## Best practices

* No obsolesce
* Don't think in GUI mode
* Prepare the reports to use before to execute
* Variables and properties
* Use jmeter functions
* Always execute the real test in a Stage of performance and using command mode
* Execute some threads to test locally

## Jmeter elements 

1. **Test plan:**  Is the element that contains the configuration and elements necessary to execute the test

2. **Thread group:** It the root element that contains samplers, controllers and go on and on. This is considered the beginning point of a test plan.

3. **Controlers:**
 
 3.1. **Samplers:** Are different types of requests send by the thread group

   - FTP
   - HTPP
   - JDBC 
   - SMTP 
   
 3.2. **Logic controlers:** Let you customize the logic that JMeter uses to decide when to send requests.
 
  - Once Only Controller
  - Interleave Controller 
  
4. **Listeners :** Show the results of test execution, is like the reporting

Listeners provide access to the information JMeter gathers about the test cases while JMeter runs. The Graph Results listener plots the response times on a graph

5. **Configuration elements:** Here we put variables, defaults variables 

6. **Assertions:** The way to validate the response, body, headers, time, status code of each test

Assertions allow you to assert facts about responses received from the server being tested. Using an assertion, you can essentially "test" that your application is returning the results you expect it to.

7. **Timers:**

By default, a JMeter thread executes samplers in sequence without pausing. We recommend that you specify a delay by adding one of the available timers to your Thread Group

8. **Pre-Processor Elements**

A Pre-Processor executes some action prior to a Sampler Request being made.

9. **Post-Processor Elements**

A Post-Processor executes some action after a Sampler Request has been made

10. **Execution order**

  1. Configuration elements
  2. Pre-Processors
  3. Timers
  4. Sampler
  5. Post-Processors (unless SampleResult is null)
  6. Assertions (unless SampleResult is null)
  7. Listeners (unless SampleResult is null)

# Using Variables to parameterise tests

Variables don't have to vary - they can be defined once, and if left alone, will not change value

HOST             ${__P(host,www.example.com)}
THREADS          ${__P(threads,10)}
LOOPS            ${__P(loops,20)}

## Trips

- Use Console to developers in Chorme or Firefox to view and debug the transactions

## Usefull commands

<code> jmeter -n -t testfile  -l file.jtl -e -o report-output/report </code>
