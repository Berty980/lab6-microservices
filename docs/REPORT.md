# REPORT
### - The two services `accounts (2222)` and `web` are running and registered (two terminals, logs screenshots).

![img.png](img.png)

### - The service registration service has these two services registered (a third terminal, dashboard screenshots)

![img_1.png](img_1.png)

### - A second `accounts` service instance is started and will use the port 4444. This second `accounts (4444)` is also registered (a fourth terminal, log screenshots).

![img_2.png](img_2.png)

### - What happens when you kill the service `accounts (2222)` and do requests to `web`? Can the web service provide information about the accounts again? Why?
We have both `accounts` services registered
![img_3.png](img_3.png)

We kill `accounts (2222)` (Uptime is 0 because I need to restart `registration` service to make `accounts (2222)` disappear from the dashboard)
![img_4.png](img_4.png)

Web still answers requests after killing `accounts (2222)` service
![img_5.png](img_5.png)

The web server can provide information about the accounts because Eureka looks for an available accounts service, it doesn't get stuck with the first `accounts` service registered

