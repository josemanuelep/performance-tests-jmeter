# Performance test in Apache Jmeter

## What is performance testing?

Is a non-functional testing approach to ensure that the application and the isolated elements of it will perform well under expected workload. 

— The goal is not finding bugs, but to eliminate performance bottlenecks of the app 

The performance testing get the measure of: 

1. Speed
2.Scalability  
3. Stability 

## Plugins

1. [Blazemeter](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)

2. [HarJemeter](https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)

## Important notes

1. Don't execute performance test using GUI mode
2. Don't execute performance test trough VPN
3. Always use a performance Stage tu execute test

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

## Different languages to use Jemeter

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

## Trips

- Use Console to developers in Chorme or Firefox to view and debug the transactions

## Generate Reports 

<code> jmeter -g generatedReport -o </code>
