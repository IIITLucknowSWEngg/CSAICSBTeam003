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

