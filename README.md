# Performance test in Apache Jmeter

Examples while learning jmeter

- [Jmeter](https://jmeter.apache.org/)

## Plugins

1. Plugin Bad Boy to record interactions on a page

- [BADBOY](opensource-demo.orangehrmlive.com)
- (Blazemeter)[https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi]

## Importants notes

- Dont execute performance test using GUI mode
- Dont execute performance test trough VPN
- Always use a performance Stage tu execute test

## State codes HTTP to use assertions

- 404 Bad request
- 200 OK
  
## Correlational dynamic values

- Sessions IDS
- Tokes and keys
- State context of application
- Others values
  - Ids
  - Objects
  - Dynamics values to test

## Differents languages to use Jemeter

Use one depent of the context

- Javascript
- Commons Jexl
- Groovy (OOP)

## Best practices

- No obsolence
- Dont think in GUI mode
- Prepare the reports to use before the execute
- Variables and propiertes
- Use jmeter funtions
- Always execute the real test in a Stage of perfromance and usign command mode

# Generate Reports 
- jmeter -g ReporteQueSeGeneraDesdeLaEjecucion -o CarpetaDondeSeGuardaraElReporte
  
