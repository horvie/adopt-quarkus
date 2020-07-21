## Higher developer productivity and more reliable applications with Quarkus

### About our company

At [Artes](https://www.artes.si/) we have been creating top-quality software solutions tailored to users for more than 25 years. Using modern approaches and state-of-the-art technology, we believe in the principle that nothing is impossible in software development.
We specialize in developing solutions for companies with large process systems, where the need for efficient and systematic operation is necessary and solutions more demanding.
Primary activities of the company:
- integration of business and process systems
- intranet applications for the control and management of technological systems
- automatic statistical data processing (gathered from the process system)
We cater to a wide range of customers from the energy and utility sectors.

### Journey into Quarkus

For many years we have had traditional server/application architecture, with several monolithic applications deployed on a single Java EE server. Applications were manually deployed to testing, staging and production environments; which was time-consuming, to say the least. Also, comprehensive test execution automation was difficult to achieve. What is worse, there were cases where memory leaks from one application shut down the entire application server, which caused the failure of other applications as well.
The nature of our work is such that we have to respond quickly to change, with as little downtime as possible. Established development and deployment cycle was no longer satisfactory; the need for improvement was great.
We have already built some prototypes with Thorntail and we liked the direction it was headed.
When we heard of Quarkus, it had the potential to be even better. 
We didn’t go down the path of full-blown microservices. First, we broke up monoliths into individual services and still deployed them to the same application server. Then we incrementally migrated individual services to Quarkus. Instead of one application server containing multiple services, we now have multiple standalone services.

### Quarkus benefits

There are several reasons to choose Quarkus and you can read about them in various articles (for starters [Four reasons to try Quarkus](https://www.redhat.com/en/resources/four-reasons-to-try-quarkus-checklist)). We are mainly focused on productivity and reliability. 
Quarkus is built on top of well-known technologies, most of which you have already used if you have a Java/Jakarta EE or MicroProfile experience, so there is a small learning curve.
It comes with a built-in development mode. You can update the application sources, resources and configurations. The changes are automatically reflected in your running application.
Using @QuarkusTest annotation you can easily write both unit and integration tests, with a bunch of out-of-the-box tooling that makes testing straightforward and simple.
If you write Camel applications, you will be happy to see how well Camel is integrated with Quarkus.

### Quarkus drawbacks

We understand that this is necessary for various build-time optimizations and such, but for us, it’s sometimes problematic that JDBC driver configuration _(quarkus.datasource.jdbc.driver)_ is fixed at build time. 
We have some applications that we deploy to customers who use different databases. If we deploy to application servers, we can configure DB drivers server-side and deploy a single build for all customers. With Quarkus we need multiple builds of the same application where the only difference is the DB driver.

### Quarkus future in our company

We are very pleased with the current state of Quarkus, the rapid development and the following of trends. We can say without hesitation, that Quarkus will be the first choice in realizing future projects as well.
