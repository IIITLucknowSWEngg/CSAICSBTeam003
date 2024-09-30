# Diagrams for LinkedIn Clone Project

---

## 1. Use Case Diagram

This diagram shows how users interact with the system.

@startuml
actor User as U
actor Recruiter as R
actor Admin as A

U -> (Create Profile)
U -> (Apply for Jobs)
U -> (Send Connection Request)
U -> (Post Updates)

R -> (Post Jobs)
R -> (View Applicants)
R -> (Search for Candidates)

A -> (Manage Users)
A -> (Manage Jobs)
@enduml


![Diagram](https://www.plantuml.com/plantuml/png/JT31oi8m3C3nUvyYn-yx-0goifiWZ4cznpRJmfREDaDyUxkj5O_xXVp3sYJ1ACiqAhGI8fX44J21ATyzsRXusR4lgDtaUGMjb8734VxQI2W4NGo37-c_g9xdyGr3tZY5Mwfw8NRG1cQouWFd4y-5ajHn5vA0cLtkvHNLVt6F5BXwUi7QznPPAkSsHllOJhR8pjUAtgPdPBpJzeyPVwsq6sANt-83 "PlantUML Diagram")


## 2. Class Diagram

This diagram shows the classes and their relationships for our system.

@startuml
class User {
  +String name
  +String email
  +String password
  +uploadResume()
  +sendConnectionRequest()
}

class Profile {
  +String bio
  +List<Skill> skills
  +updateProfile()
}

class Job {
  +String title
  +String description
  +applyForJob()
}

class Recruiter {
  +String companyName
  +postJob()
}

User "1" -- "1" Profile
User "1" -- "0..*" Job : applies for
Recruiter "1" -- "0..*" Job : posts
@enduml


![Diagram](https://www.plantuml.com/plantuml/png/TP1FImCn4CNl-od2dln3Yrv5f21u417PuWT8awaCJZ8nCq6A-DrjrY1PeQTXNZBlztWRKPkr11eSMH7pAf3Drs3CvLOpnZSJRO1kXM2HkZrPaK_Elaeb4Li_WPG0P-TL4OZ-dcC4fyXnWey2eiUdxw7XNZBlaM11t27NxGb5RxVlI7Hdf0xvPNYhqCvwfqVUBLmKbVhW7iHbJ3L7LMrAT7ZWV3phNIPmkQ3-wy1nI3OUdbiLYKN_xkR2nklHh5RpQD6M-jLwVJ7E4MzC9IE8sNCU6kx4pygHOGFHbq0_)


## 3. Sequence Diagram

This diagram shows the process flow when a user applies for a job.

@startuml
actor User
participant "Job Portal" as JP
participant "Job" as J
participant "Recruiter" as R

User -> JP: Browse Jobs
JP -> J: View Job Details
User -> J: Apply for Job
J -> R: Notify Recruiter

R -> J: Review Application
J -> User: Confirm Application Status
@enduml


![Diagram](https://www.plantuml.com/plantuml/png/POqzJWGn34PxdyBQdWjCWPQVQWeq2eBU18zaAHD7ZiDgRyzw1n28zZs_pyVkP3ws0fHT3Lyw6pGobooDgkDXrZTSr9pA0QdZlFpJE_-B4sSRucnNcG1Y66zkB_s4zwQdpdX9EypBbKxuAdmAX8_i9AL_5-7kMYjdNDNY0EQWQS8dTLdF-FCA87tT9_w8jSWaaulMFOh92H-qhcBRRutFJZuw7Bc-Zwry0W00)

## 4. Activity Diagram

This diagram represents the flow of actions for sending a connection request.

@startuml
start
:User logs in;
:User searches for connection;
:User sends connection request;

if (User already connected?) then (yes)
  :Show "Already connected";
else (no)
  :Send request notification;
  :Wait for response;
  if (Request accepted?) then (yes)
    :Add to connections;
  else (no)
    :Show "Request declined";
  endif
endif

stop
@enduml

![Diagram](https://www.plantuml.com/plantuml/png/RP1BRiCm34JtF0MHbNE5UD7a2YsAhWLfN0jGILTaKEJszSSkX28RGIHdD4-yceVgzwz2wuKkxuRAHJ-Di_HxQGWrZZ0Uj79K4KJFsembMTFdYkyxp7kYF72tQaAf2Ebng91UpkmZXBi7x4pCbxTHV_Xq-wyxzOHYu4vqaq7I4S2YdeSSmqOpJpz2zfMomYOLmz9T85vtHuWHqvFusNjBYLsRVzXYRiF_A8_N4cB9ia8oGr8UQ3l9N2UwpiMysby0)


## 4. Architecture Diagram

This is a basic system architecture diagram, showing components of your LinkedIn clone.

@startuml
node "Client" {
  [Web Browser]
  [Mobile App]
}

node "Server" {
  [Web Server]
  [Application Server]
}

node "Database" {
  [User Data]
  [Job Listings]
}

[Web Browser] --> [Web Server]
[Mobile App] --> [Web Server]
[Web Server] --> [Application Server]
[Application Server] --> [User Data]
[Application Server] --> [Job Listings]
@enduml

![Diagram](https://www.plantuml.com/plantuml/png/VP2_2i8m4CRtFCNHlQyWzSyaEeauI8V47d8Gat9twY2-kst9S4LnlE_xVkH76b7FUhz5btA7KAqZOT8ANWxWVC80AyvFGMx7Uvy3HOHbtxVkxGfnG7uW6s8C2Z0i8rsyKaubDk36gmzUiA17GOOncyXj3h0ZKKfNcPYP3DJrOlwOTVjkpL7QNsOsj6lhzcSqLsumTSEtVW00)


