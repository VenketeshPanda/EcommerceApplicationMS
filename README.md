# Ecommerce Application Microservice 
This is collection of all the microservices I built for an Ecommerce application


**Product service:** 
- This service acts as the inventory, we can store, retrieve and modify the products based on the need.
- Made use of caching using Redis and improving latency by 100x.
- Used Flyway for all the schema migrations.
- It acts as a Client LB for User service for the request that has to go through the product service.
- Configured Prometheus for all the metrics visualization.
- Added Dockerfile to containerize and deploy the application quickly. 
- Link to the repository: https://github.com/VenketeshPanda/ProductService


**User service:** 
- This service acts as the user base of the project. 
- All the signup, login and logout functionalities are implemented here.
- I have used Spring Security and implemented OAuth2 for authenticating the users.
- Also acts as a producer to trigger an event to send email notification whenever a new user signs up.
- Link to the repository: https://github.com/VenketeshPanda/UserService

**Payment service:**
- Integrated Stripe and Razorpay payment gateway for payments.
- Link to the repository: https://github.com/VenketeshPanda/PaymentService

**Notification service:**
- This acts like the consumer whenever userservice triggers a sendEmail trigger, it captures it and sends an email to the concerned person.
- Link to the repository: https://github.com/VenketeshPanda/NotificationService

**Eureka server:**
- This acts as a service discovery.
- This service maps all the available instances of the registered services, which our API gateway can use to redirect the requests and balance the load.
- Link to the repository: https://github.com/VenketeshPanda/EurekaServer
