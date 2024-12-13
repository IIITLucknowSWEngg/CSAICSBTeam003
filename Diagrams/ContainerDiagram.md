### **C4 Container Diagram for LinkedIn Clone**

Below is the **C4 Container Diagram** for the LinkedIn Clone project. This diagram represents the key components of the system, focusing on Recruiters and Job Seekers as primary actors. It illustrates the structured hierarchy, showcasing the Frontend, Backend, Database, and Cloud Services layers, and how these components interact.

---

### **Diagram**

![Container Diagram](https://www.plantuml.com/plantuml/png/fLHFJ_j64BtxKymlfo11N5MSUeA6yASAa68GnsXjJvAbwrrtPnsJLltkdR53OWihgbGksHdFl3TlzmrN59GFLM6Y7pckj4MONawT3OgFFlgXRMQg764JGac_nB5NzMIjmwPAAqAVSI7QCCbS4PT6MS6ve90RdSRJouk5fDuUvt6XAA3drF80FIc5CrgW9sV70dOEepV-6V7lDPJUhP18EwiCr1i7N44mr_OFp1yiJ8sp2C51eQnQysc3sZTDsY0ecmEFPZ4Baz5PbEoOlLZ-wYgRAxyRcmP5ssKcA4pNXnsTmTyHyDzXrd6DwLAL9PU-OmhNPMbqfW8F9yE-e6AU3se6DyRL12A7P3njMJT_XfhlJAQ4qgYmShw0hLQGUbTBgKpPPonSoahsf8zDCCWBJnnlKUAPLQd13hdACgHlb-OijE2GurPdE42kIhrSgu2rseccnGFSjP7GFBaSMMqy-omzmpUJk2eWDTTEc5MS1cdo-6U550O93agMX5x64A9Z5f8sso6KuprJYCJCUGHseBOYqBYrpXfsaGwv2kexfMHJHS9pipyAui9HM7jCVfzBb0G6fYFC-Tv6CXATDnIb6rI4XTAcesKcSLT5WZQ_yph_EXDWKs9TqAkzwkRLgc53g2fikdV58TemS5tFyWb-dlmamQEinvSYrUyHDP9oNl_LPBwJbcfNS4U7Tz5cUig2roLsdwVqMEYg0AfIolXZgqtuze03-ZwSh9XcbDzSAlPfBFqPq5jblkA5TrkTCmDNWz4Kj5stm1wD2fWV7l-VA7f1i_-_SbpVDyBMIA-lYuJBZZMTXHikEu3qjqFUic_tPYDcoMlSxMxX_mT0hsbuVswThvN_Rs03_PqDUK6LK_pkTK0wrT9p_GbZdmJfEhjZehvRJm4CkDIx38cG-XOy1NBqtos6RBFtcDm9TqN9_VFxSZwxcptTZC-YAvPP5UPV)

```plantuml
@startuml
!define C4Container
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(user, "User", "A professional who uses LinkedIn Clone to manage their profile and connect.")
System_Boundary(linkedin_clone, "LinkedIn Clone") {
    Container(web_app, "Web Application", "React.js", "Allows users to interact with the platform via browsers.")
    Container(mobile_app, "Mobile Application", "React Native", "Enables users to access LinkedIn Clone on mobile devices.")
    Container(api_gateway, "API Gateway", "Node.js/Express", "Routes and secures API requests.")
    Container(application_service, "Application Service", "Node.js", "Handles core business logic and user data.")
    Container(database, "Database", "PostgreSQL", "Stores user data, connections, and posts.")
    Container(email_service, "Email Service", "SendGrid", "Sends email notifications to users.")
    Container(auth_service, "Authentication Service", "OAuth 2.0", "Manages user authentication and authorization.")
    Container(payment_service, "Payment Service", "Stripe", "Handles premium subscriptions and payments.")
    Container(job_api, "Job API", "External API", "Provides job listings and related data.")
}

Rel(user, web_app, "Uses", "HTTPS")
Rel(user, mobile_app, "Uses", "HTTPS")
Rel(web_app, api_gateway, "Sends API requests", "REST/HTTPS")
Rel(mobile_app, api_gateway, "Sends API requests", "REST/HTTPS")
Rel(api_gateway, application_service, "Forwards API requests", "REST/HTTPS")
Rel(application_service, database, "Reads/Writes")
Rel(application_service, email_service, "Sends email notifications")
Rel(application_service, auth_service, "Handles authentication")
Rel(application_service, payment_service, "Processes subscriptions")
Rel(application_service, job_api, "Fetches job data")

SHOW_LEGEND()
@enduml
```

---


### **Description for C4 Container Diagram**

The C4 Container Diagram illustrates the main components of the LinkedIn Clone project and their interactions. It outlines how the system is broken down into containers (applications and services) and the responsibilities of each component.

- **User:**
  The User interacts with the system through either the **Web Application** or **Mobile Application**, enabling access to LinkedIn Clone’s features such as profile management, networking, and job search.

- **Frontend Layer:**
  - **Web Application:**
    A React-based application that users access via browsers. It allows them to interact with the platform, manage their profiles, post content, and connect with others.
  - **Mobile Application:**
    A React Native mobile app that provides similar functionality as the web app but optimized for mobile devices, allowing users to stay connected on the go.

- **API Gateway:**
  A Node.js/Express-based service that acts as a reverse proxy to route incoming requests to the appropriate backend services. It ensures that requests are properly secured and forwarded to the correct containers.

- **Application Service:**
  A Node.js service that implements the core business logic of the platform. It processes requests related to user management, connections, job listings, posts, and notifications.

- **Database:**
  - **PostgreSQL Database:**
    Stores structured data such as user profiles, job postings, connections, and messages. This relational database is optimized for storing and querying user-related information.

- **Email Service:**
  Utilizes an external service (e.g., SendGrid) to send email notifications to users for various events, such as job applications or new connection requests.

- **Authentication Service:**
  Uses **OAuth 2.0** to manage user authentication, ensuring that only authenticated users can access the platform and interact with its features securely.

- **Payment Service:**
  Integrated with **Stripe**, this container handles transactions related to premium subscriptions and payments for enhanced user experiences or job-related features.

- **Job API:**
  An external API that provides job listings and related data, enabling job seekers to browse opportunities and apply for jobs directly through the LinkedIn Clone platform.

Each container is designed to handle specific parts of the system's functionality, making the LinkedIn Clone scalable, maintainable, and flexible. The containers communicate with each other through APIs and message queues, ensuring smooth interaction between different components of the platform.
