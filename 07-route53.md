# Amazon Route 53

Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. You can use Route 53 to perform three main functions:

**Register domain names**
Your website needs a name, such as example.com. Route 53 lets you register a name for your website or web application, known as a domain name.

**Route internet traffic to the resources for your domain**
When a user opens a web browser and enters your domain name (example.com) or subdomain name (apex.example.com) in the address bar, Route 53 helps connect the browser with your website or web application.

**Check the health of your resources**
Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functional. You also can choose to receive notifications when a resource becomes unavailable and choose to route internet traffic away from unhealthy resources.

# Routing Policy
When you create a record, you choose a routing policy, which determines how Amazon Route 53 responds to queries:

- Simple routing policy – Use for a single resource that performs a given function for your domain, for example, a web server that serves content for the example.com website. Randomly pick an IP from the list.

- Failover routing policy – Use when you want to configure active-passive (primary-secondary) failover. 

- Geolocation routing policy – Use when you want to route traffic based on the location of your users.

- Geoproximity routing policy – Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another.

- Latency routing policy – Use when you have resources in multiple AWS Regions and you want to route traffic to the region that provides the best latency.

- Multivalue answer routing policy – Use when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random.

- Weighted routing policy – Use to route traffic to multiple resources in proportions that you specify. For instance 20% and 80%.
