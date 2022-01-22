# Team-13 Project

## Purpose
The purpose of this application is to create a webapp that handles booking dentist appointments and searching for clinics. These clinics will be visualized through an interactive map. The team working on this project are as follows:
- Mattias Schaurig - Scrum Master
- Nils Dunlop - Product Owner
- Albert Simpson - Developer/Meeting Responsible
- Ivan Alexis Pena Mercado - Developer
- Mislav Milicevic - Developer/Coder Consultant
- Younis Akel - Developer/Trello Responsible
- Enes Akin - Developer



## The relevant resources are as follows:
### Trello:
   * https://trello.com/invite/b/j3mTLiHn/a4e26295e41a189df26e26383e76f3c0/dit-355-2021-team-13
## Repositories:
### Clinic Registry
   * https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/clinic-registry
### Booking
   * ttps://git.chalmers.se/courses/dit355/test-teams-formation/team-13/booking
### RESTful API
   * https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/rest-api
### Client:
   * https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/frontend
### Local-Infrastructure(Docker container containing local MQTT Broker & MongoDB for development purposes):
   * https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/local-infrastructure

## Getting Started
### Step 1
First of all clone all the gitlab repositories.
- [Frontend](https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/frontend )
- [Booking](https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/booking.git)
- [Clinic Registry](https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/clinic-registry)
- [Rest Api](https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/rest-api.git)
- [Local Infrastructure](https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/local-infrastructure.git)

### Step 2
Follow instructions to set up mqtt broker and mongoDB database via a docker component from the link below
https://git.chalmers.se/courses/dit355/test-teams-formation/team-13/local-infrastructure/-/blob/master/README.md

### Step 3
Open the local infrastructure repository in a terminal and run the below commands to set up the Mongo database and MQTT broker.
`cd [Your System Files]/local-infrastructure`
`docker compose up`

### Step 4
To set up all of the components, open a separate terminal for each of them and enter the following commands:
`npm install`

### Step 5
To run the backend open up the rest-api, booking and clinic-registry components in separate terminals enter below command.
`npm run dev`

### Step 6
Lastly to run and view the frontend open the frontend component in a terminal and do the following.
`npm run serve`

Now everything should work as intended! Hope you enjoy our dentist booking project 😃

### Common issues
The ports 3000, 3001, 3002 and 8080 are already in use. Hence, if other processes (or one or more components are already running) are using these ports an error will occur. The solution would be to end the processes using the port(s) or to modify the port(s) that the project is using.


## Software Requirement Specification (SRS):
### User Stories
1. As a developer I want to have a basic backend and frontend template so that I can start working on coding features.
   * https://trello.com/c/fV2HzDML/15-1-setup-node-vue-project
1. As a developer I want to be able to retrieve clinic data from a JSON webpage so that this can later be applied to map the clinics in Gothenburg and can also be used by other components.
   * https://trello.com/c/DjLZxYdZ/20-2-read-dentist-clinic-registry
1. As a user, I want to have a visual map of Gothenburg, so that I can see all available dentist clinics within the City.
   * https://trello.com/c/eZeBpFxQ/17-3-map-of-gothenburg-in-user-interface
1. As a user I want to be able to search for clinics so I can find the clinic I want and be presented with it's related information.
   * https://trello.com/c/ByHHoWJQ/24-4-clinic-search
1. As a developer I want to be able to connect the clinic registry component to a database so that the other components can retrieve clinic registry information.
   * https://trello.com/c/U86E9Vdk/31-5-clinic-registry-database-handler
1. As a developer I want to have a RESTful API for the clinic registry component, so that the client  is able to retrieve data on clinics.
   * https://trello.com/c/E5Op9uwx/35-6-restful-api-clinic-registry
1. As a user, I want every user booking endpoint to be connected and communicating with MQTT so that booking data can be sent to the webpage.
   * https://trello.com/c/EL67kjtq/32-7-mqtt-booking
1. As a user, I want the system to process my booking request, so that I actually book with a clinic.
   * https://trello.com/c/pqD2Qghd/21-8-user-booking-request-to-backend
1. As a developer I want to be able to connect the RESTful API to a MQTT broker so that the client using the RESTful API is able to connect to the server.
   * https://trello.com/c/wWytXnTE/22-9-mqtt-restful-api-booking
1. As a developer I want to have the MQTT communication be implemented so that the booking component can communicate with the client through RESTful api.
   * https://trello.com/c/o5OTFICH/33-10-booking-feature-backend
1. As a user I want to be able to book appointments to the dentist so I can check up on my teeth.
   * https://trello.com/c/HpVh4M9h/16-11-booking-feature-frontend
1. As a user, I want to be able to receive directions to dentist places using different transport modes so that I can plan my dentist trip better.
   * https://trello.com/c/0mohYDmF/46-map-directions
1. As a user, I want to be notified of errors in a simple way so I can understand when something goes wrong in the system.
   * https://trello.com/c/9uIEcaLN/29-13-frontend-error-handling
1. As a developer, I want the dentist registry component to check for updates regularly, so that the correct information is displayed to clients
   * https://trello.com/c/Fw71xlmI/40-20-dentist-registry-update-tracker
1. As a user, I want to be given a page with all booking data after confirming the booking stage so that I know when my dentist appointment is taking place.
   * https://trello.com/c/Y0PWlzIl/34-15-booking-system-response
1. As a developer, I want to have CI to test that the clinic registry component code functions as expected, so that I know the new code I am introducing will not break the system.
   * https://trello.com/c/OGJ6IxvV/36-16-ci-for-clinic-registry-component
1. As a developer, I want to have CI to test that the booking system component code functions as expected, so that I know the new code I am introducing will not break the system.
   * https://trello.com/c/y5EYsM9d/37-17-ci-for-booking-system-component
1. As a developer, I want to have CI to test that the Restful API component code functions as expected, so that I know the new code I am introducing will not break the system.
   * https://trello.com/c/v4dFnygy/38-18-ci-for-restful-api-component
1. As a developer, I want to have CI to test that the client component code functions as expected, so that I know the new code I am introducing will not break the system.
   * https://trello.com/c/15NKUutZ/39-19-ci-for-client-component
1. The Map system component in the component diagram has been replaced with a "Clinic Registry System" component instead. This component should be updated in the component diagram.
   * https://trello.com/c/QImPky56/41-20-update-component-diagram-with-clinic-registry-component
1. During the development of the clinic registry system component (task 5), a component diagram was created to act as a guideline to the code structure. This should be added to the documentation
   * https://trello.com/c/BXoxYSOj/42-21-detailed-clinic-registry-system-component-diagram
1. During the first sprint, an initial documentation (use case diagram, component diagram, requirements etc) were created. These should be added to initiate the documentation repository.
   * https://trello.com/c/7mCJ0Tm5/43-22-initiate-documentation
1. The initial plan for each component having its own database was switched to having a single shared database as @dekmm suggested. This should be reflected in the component diagram.
   * https://trello.com/c/gY5v4mAk/44-23-update-component-diagram-with-database-structure-change
1. It was decided  that registration and login (account feature) is out of scope. Hence, this change should be reflected in the use case diagram
   * https://trello.com/c/yMRZEIUB/45-24-use-case-diagram-update
1. As a developer, I want to have restAPI endpoints, so that the frontend can request available appointments
   * https://trello.com/c/Ze8PYoZf/51-25-appointment-availability-rest-api
1. As a developer, I want the two components rest-api & booking to have a validation before and after going through the broker to ensure the messages are validated so that the messages won't cause issues or crashes to the components.
   * https://trello.com/c/2JFBSfOf/53-26-booking-validation
1. As a user, I want the website to have a home screen so I can view the map and search for clinics.
   * https://trello.com/c/y1nmdCq6/52-27-home-screen
1. As a developer, I want there to be a circuit breaker in the booking component, so that the system is fault tolerant towards too many booking requests in a given time.
   * https://trello.com/c/hd0LFYqn/65-28-circuit-breaker-booking-component
1. As a user, I want to be able to confirm a dentist booking in the clinic screen so that I can check that my teeth are healthy.
   * https://trello.com/c/i7g79GeV/66-29-connect-bookings-to-the-dynamic-clinic-screen
1. As a developer, I want the REST API to know if the circuit is open, so that the user is notified if the booking system is unavailable
   * https://trello.com/c/4zNpnlgw/68-30-circuit-breaker-restful-api
1. As a user, I want a message to be displayed to me when the system is overloaded, to know that my booking request was not processed.
   * https://trello.com/c/HY4uqWsJ/70-31-circuit-breaker-displayed-to-user
1. The component diagram should be updated with the circuit breaker that was recently added to the booking component and the status checker added to the Rest API component
   * https://trello.com/c/OLB70Q7W/71-32-update-component-diagram-with-circuit-breaker

## Software Architecture Document (SAD):
### Publish & Subscribe
The publish and subscribe architecture style is used to enable components to communicate with each other in a manner that ensures distributed transparency. This architectural style allows us to design our system in an event driven manner (ie if a user makes a booking, we consider that to be an event). Furthermore, this also enables scalability, as adding more components would be able to communicate with the rest of the system by subscribing/publishing to topics, hence simplifying the integration process.

### Client & Server
The client and server architecture style is used within our components to communicate between our frontend web page and backend server. The communication between the components will be done by the broker and the client will use a RESTFUL API.

### Microservices
The microservices architecture style is used to ensure a decoupled system. This is done by having a collection of independent components with no shared memory communicating through messages. In addition, this assists in scalability since new components would not interfere with other components and functions independently.

### Pipe and Filter
The pipe and filter architecture was used in combination with the pub/sub architecture. We used this design decision to incorporate one-way processing in the system. An example of this would be the filtering happening in the booking component. An MQTT message contains two properties being method and data, data containing the request body and method being the indicator of what kind of HTTP method used. When handling a booking in the contorller we do not care about the method property in the MQTT message thus we filter it out right before the data from the request body gets handled by the logic in the controller.

## How is the conceptual design mapped onto implementation/technologies

### Publish & Subscribe
Ín our implementation, the publish and subscribe architecture style will be used between the client and the booking backend with the communication of MQTT. This style assists us in being able to continuously update the availability of the dentist bookings.

### Client & Server
In our implementation, we have a client, namely the frontend, which decouples from the server, namely the backend. These two components are separated and don’t rely on one another to function. We have implemented them so that they communicate with each other through a middleware, namely the RESTful API which then sends messages to an MQTT broker.

### Microservices
In our implementation, each component acts as a microservice, as they all provide their own unique service.


### Pipe and Filter
The pipeline and filter architecture maps to our implementation in terms of providing one way processing. In our case, the MQTT middleware would act as the pipe, and the different components would contain filters and testers that manipulate/check the incoming data. For example, if a Booking request is sent from the RESTapi to the Booking component, it would be sent via mqtt (pipe). This booking request would then go through transformer and tester filters in order to be processed by the booking component.

### Technologies
Deciding the design conception for the frontend client has let us understand the needs for the technologies that will be needed, vueJS, Axios, Google Maps Library API. Knowing what type of backend server we are going to work with lets us realize the requirements we need for the technologies used for the development. These technologies for the backend server are ExpressJS, NodeJS, and Mongoose for the mongoDB.

## Program Management Report (PMR):
For the project management practices, we are following scrum & kanban practices. We have biweekly sprints, that includes the following meetings: sprint planning, sprint review, and sprint retrospective. We also have a standup after half of a sprint has been completed to check up on “What you have done?”, “How is it going?”, “What do you plan to do?” “Is any assistance needed?”. For our requirements management, we use a kanban board on trello that is updated regularly to reflect the current state of the project/requirements.

### Team agreement:
### Roles:
- Scrum Master - Mattias
- Product Owner - Nils
- Developers - All


### Functions:
- Meeting Agenda Planer/Responsibility - Albert
- Delivery Responsibility - Nils
- Trello Responsibility - Younis & Miso
- Reviewer - All


### Meeting Schedule:
- Monday 14:00 - Sprint Planning/Mid Sprint Standup
- Friday 17:00 - Sprint Retrospective


### Code of Conduct:
- Everyone is expected to do their parts and fulfill their roles
- It is okay to have one or two weeks worse performing, just make sure it doesn't get across the entire course
- If you have a rough time then make sure to communicate it and settle it with everyone
- Be respectful
- You're expected to be on time and have your things you need to do done
- Otherwise message or notify before about any hindrances

## Diagrams

### Conceptual Diagram
![Conceptual Diagram](images/conceptual_diagram.png)

### Use Case Diagram

![Use Case Diagram](images/usecase_diagram.png)

### Component Diagram
![Component Diagram](images/component_diagram.png)

### Detailed Clinic Registry System Component diagram
![Detailed Clinic Registry System Component Diagram](images/detailed_clinic_registry_component_diagram.png)

**Mapping of the "Detailed Clinic Registry System Component diagram" to the actual code:**

The main architecture style/pattern used here was the "pipeline and filter". This was chosen as one-way processing was required, and the data would mainly flow in a specific direction. In this case, we can see the data flow through a pipeline that starts from the external registry interface and ends at a mongoDB database. These components generally map directly to the code files. Ie, there is a JsonComparator.js file that compares the json data etc. The components would correspond to the following filters:

* **Producer:** Registry Reader - This component calls/retrieves clinic data from the external clinic registry. This component initiates the pipeline process.

* **Tester:** The JsonComparator retreives data from the external registry, and compares this to the existing database data. If there is a difference, the data will move into the next filter in the pipeline.

* **Transformer:** The DBUpdater component is considered a transformer in this case, as it converts the data (by using mongoose) to a suitable format so that it can be stored within the mongoDB database.

* **Consumer:** The mongoDB database would be the consumer in this case. This is because it would act as the termination point of the pipeline data flow.


## Component diagram change log:

### Clinic Registry System replaces Map System during sprint 2:

The reasoning for this is that we wanted to have a single component that the other components receive data from. We also wanted to ensure that any updates to the registry would also be made known to the system. Hence, this new "Clinic Registry System" component was added. We decided to instead remove the Map system, as the map was anyways contained inside of the client.

### Circuit Breaker related components are added during sprint 4:

The circuit breaker was added according to the project requirements. This addition can be seen in the "Booking system" component, where a "System Overload Handler" component was added (along with its nested components). The "RESTful API" component was also updated by adding a "Circuit Breaker status checker" component to the nested "Booking controller" component.

## Use case diagram change log:

### Unique booking codes replaces user accounts during sprint 2:

Our reasoning for this is that we wanted to simplify our process by not needing to have a component solely dealing with users i.e. registration and login. Instead, our workaround for this is to provide users with unique booking codes upon booking a dentist appointment. Using this booking code users could view, update and delete their bookings. In addition, we replaced the clinic registration with an available bookings search since it felt more appropriate with the number of clinics our system is going to handle.

## Final Video
[![Final Video](https://img.youtube.com/vi/hzl2m16k808/0.jpg)](https://www.youtube.com/watch?v=hzl2m16k808)
