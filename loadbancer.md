OCI Load Balancer


 
 
I'll explain the 

- concepts and features of OCI load balancing service
- public and private load balancers
- policies and the health checks

let's start our discussion with what is the load balancer or what does it offer? 



![image](https://github.com/chrahul/OracleCloudConcepts/assets/14847377/478ce01c-ff9f-4bbf-9e83-261a70f9d421)





It basically sits between the clients, your users, and the back-end servers. So these back-end servers are actually the servers that you're going to be providing the service with, only that the load balancer will sit in front of them specifically for doing that, balancing the load.

So what are the tasks performed by the load balance? So basically, it does service discovery, do health checks on the health of the servers, makes sure that they're up and running. If they're not, they'll take them out. And the algorithm that you're going to be using to reach those servers, for example, Round Robin ITHash, other services that you might utilize besides those two.

So basically, you get the requests, they reach the load balancer, and then the load balancer distributes the loads across your servers. Again, if one of them goes down-- you have four in this image. If one of them goes down, then you have three because it will completely take that server out of service.

So benefits from the load balancer? One of them is that you distribute traffic across all of your servers in a way that you specify and also provide you with high availability because if one goes down, the service keeps on going. You still have fault tolerance.

You can scale. Basically, you can set policies on your load balancer for automatic scaling and combine that with that service, in case you don't receive the traffic that you're expecting, so you don't need to be paying for four servers in this case of the example. If you can serve these traffic that you're receiving with two servers, then you can decommission two of them. If you see traffic increase where a threshold is reached on your servers, let's say that they're at 80%, each one of these servers, so maybe you need a fifth server to handle the oncoming traffic.

And then naming abstraction. Basically, you can hide the actual names and just use the name from the load balancer and the name could be the IP address associated with it.

So what services that you gain from the Oracle Cloud Infrastructure load balancing as a service? So basically, high availability and scalability. As we explained previously, you can scale based on the need, and by having the load balancer, you have high availability by nature. If one of them goes down, the service continues running.

So the load balancer enables public and private load balancer options. That means that if you have a public load balancer, that means that you get a public IP address for it. If you don't, if you set it up as a private, then you will not be getting a public IP address, because that's the nature. You want the load balancer to balance private resources.

It supports protocol TCP, HTTP/1.0, 1.1, HTTP/2, and WebSocket as well. Now, you can terminate SSL on it end-to-end, and you can also enable SSL tunneling. It supports advanced features like session persistence and path based routing.

Now, the key differentiator from the Oracle Cloud load balancing of service is that you can establish private or public load balancer with public IP address, and you can provision the bandwidth. You can set a specific bandwidth or you can have a flexible load balancer.

Now a single load balancer can enable TCP layer 4 and HTTP layer 7 traffic. Oracle just released a TCP specific load balancer. In case you want to combine both services, then you can use HTTP and TCP on one load balancer. If you want a load balancer specifically for TCP traffic, then you have that option with Oracle Cloud Infrastructure.

So let's see the fixed and the flexible options in more detail. With the fix shape option, you get 10, 100, 400, and 8,000 megabits per second, shapes, and they're fixed. That's what you're going to be getting from the moment you select going forward. 8,000 of course meaning 8 gigs.

With the flex load balancer, you just define a minimum and a maximum. You can go from 10 to 8,000, but it's going to be flexible. So you're going to be using 10 when that's what's required, and if your bandwidth requires more, then it's going to be scaling until you reach the maximum. So the minimum bandwidth will provide you instant readiness so you can start working immediately.

The maximum will allow you to maximize and keep control of your cost. Flexible. And you have faster scaling load options. So, basically, the balancers can distribute your pre-provisioned multi-tenant fleets.

The fixed to flexible load balancer. So basically, once you make a selection, and if you're on the fixed and then you start seeing the benefits or you said, OK, rather than migrating from my 10 to 100, I'm going to migrate from 10 to flexible, and there's a procedure that you have to follow and it's highlighted in this image. So basically, you make a selection and you start following this procedure.

So you can configure the minimum and the maximum that bandwidth the same to mimic what you had, basically. So if you had a 100 fixed, then you can start from 10 to 100, and that when you reach 100, it's going to mimic what you previously had.

HTTP/2 is supported on your flexible load balancer. Not on the fixed one, but on your flexible load balancer, and supports HTTP/2 for your HTTP and HTTPS listeners. And basically, this will include enhancements for your users accessing your services from their mobile devices. Thank you very much.
