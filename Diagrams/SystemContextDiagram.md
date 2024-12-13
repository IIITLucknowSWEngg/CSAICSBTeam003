## **System Context Diagram**

### **Title**  
System Context Diagram  

### **Description**  
The System Context Diagram provides an overview of how the LinkedIn Clone interacts with external actors and systems. It shows the major components of the system, including users (job seekers, recruiters, and administrators) and external services (like email notification services and databases).  

---

### **Diagram**  
![System Context Diagram](https://www.plantuml.com/plantuml/png/TP51Rzim38Nl-XMSxq6nzhR3q3Z9XWrPLoGTTbObsXKYYm55jmY2_VT9Lk9v1kgJ_Dv7Ye-wZw9P-iwh3nOR5n1sczNJyk7hTWF6wnX7VRbw-ha3ROHOgNXmuQXPTy1eH8VM8vmLfA_Mvj0ozS6ko1F3xnSdM1nYYrpKsYTiKBzGaAdsPzAyt0Rdzq2FZO0Gi6jV1ApBipWAIfMwwZizmnxnW5o1Zl0h8d-yUZiqt3kPMBTNQsax5qRvJgb_6Qkj2mUqtmAiF0M4_IaATfcz72_3JYfo3tXaQbpw-w63Rh738BdcAizByjnR5yM5TbwHh3Z77qXSuupEsLDUVdK61tWmJdbJnbDleTfqsld_a45HLej-rZ7rMfTJCTUrKiFIO67fBIm-Zpa-fIqPWt6CK5t1uIqIcGVDMCtq5l5cUJpw4pJ4Wr7eMrXuRARm8qM1IVeBU3VUNn9bjEm5fjaJNVmHBtaJlSTWvsnvi95TrmCen7YpGs67hmXv7PMwJzLzv_y2)  

---

### **Code**

```plantuml
@startuml
!define RECTANGLE class
!define ACTOR actor

skinparam rectangle {
    BackgroundColor White
    BorderColor Black
    FontColor Black
}

skinparam actor {
    FontColor Black
}

left to right direction

actor "Job Seeker" as User1
actor "Recruiter" as User2
actor "Admin" as User3

rectangle "LinkedIn Clone System" as System {
    rectangle "User Profile Management" as Profile
    rectangle "Job Listing Management" as Jobs
    rectangle "Notification Service" as Notify
}

cloud "Email Service" as Email
database "Database" as DB

User1 -down-> Profile : "Access Profile"
User1 -right-> Jobs : "Browse/Apply for Jobs"
User2 -left-> Jobs : "Post Job Listings"
User3 -down-> Notify : "Manage Notifications"
Notify -down-> Email : "Send Notifications"
System -down-> DB : "Store/Retrieve Data"
@enduml
```

---

## **Actor Interactions**

### **Job Seeker**
- Users can create and update their profiles.
- They can browse job listings and apply for jobs directly through the system.

### **Recruiter**
- Recruiters can post job listings for open positions.
- They can review applications submitted by job seekers and manage postings.

### **Admin**
- Admins oversee the management of notifications.
- They handle system-level configurations to ensure smooth operations.

---

## **External Systems**

### **Database**
- The system uses a database to store and retrieve user data, job postings, applications, and other essential records.

### **Email Service**
- The email service handles notifications sent to users, such as job alerts, application updates, and system messages.
