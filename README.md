
# REST API for an Covid-19 Application

* I have developed this REST API for a Covid-19 Application. This API performs all the fundamental CRUD operations of any COVID-19 application platform with user validation at every step.

## Tech Stack

* Java
* Spring Framework
* Spring Boot
* Spring Data JPA
* Hibernate
* MySQL
* Swagger

## Modules

* Login, Logout Module
* User Module
* Admin Module

## Features

* User and Admin authentication & validation with session uuid
* Admin Features:
    * Administrator Role of the entire application
    * Only registered admins with valid session token can add/update/delete driver or customer from main database
    * Admin can access the details of different Appointment, Member ,Vaccine Center ,Vaccine Inventory and Vaccine Ragistration.
* User Features:
    * A user can register himself or herself on the platform.
    * He/She can check the vaccine centres and vaccine availabilty.
    * If vaccine is available, can book an appointment slot.
    * After booking an appointment, he will get appointment details for the vaccine dose.    









## Installation & Run

* Before running the API server, you should update the database config inside the [application.properties](https://github.com/Aman3512/Covid-19-Vaccination-Spring-Boot-Project/blob/main/Covid_vaccination_service/src/main/resources/application.properties) file. 
* Update the port number, username and password as per your local database config.

```
    server.port=8888

    spring.datasource.url=jdbc:mysql://localhost:3306/cowin;
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=root

```

## API Root Endpoint

`https://localhost:8888/`

`http://localhost:8888/swagger-ui/`


## API Module Endpoints

### Login Module

* `POST //api/adminlogin` : Admin can login with mobile number and password provided at the time of registation
<!--
### User Module


* `POST /customer/login` : Logging in customer with valid mobile number & password
* `GET /customer/availablecabs` : Getting the list of all the available cabs
* `GET /customers/cabs` : Getting All the cabs
* `GET /customers/checkhistory` : Getting the history of completed tr
* `PUT /customer/update/{mobile}` : Updates customer details based on mobile number
* `PATCH /customer/updatepassword/{mobile}` : Updates customer's password based on the given mobile number
* `POST /customer/booktrip` : Customer can book a cab
* `POST /customer/updatetrip` : Customer can modify or update the trip
* `POST /customer/logout` : Logging out customer based on session token
* `DELETE /customer/delete` : Deletes logged in user 
* `DELETE /customer/complete/{tripid}` : Completed the trip with the given tripid 
* `DELETE /customer/canceltrip` : Cancel the trip with the given tripid   


### Admin Module

* `POST /admin/register` : Register a new admin with proper data validation and admin session
* `POST /admin/login` : Admin can login with mobile number and password provided at the time of registation
* `GET /admin/logout` : Logging out admin based on session token
* `GET /admin/listoftripsbycustomer` : Get list of trips of by a customer id
* `GET /admin/listoftrips` : Get list of trips of all the trips
* `GET /admin/listocustomers` : Get list of all the customers
* `GET /admin/listodrivers` : Get list of all the drivers
* `PUT /admin/update/{username}` : Updates admin detaisl by passed user name
* `DELETE /admin/delete` : Deletes the admin with passed id   -->


### Sample API Response for Admin Login

`POST   localhost:8888/login/adminlogin`

* Request Body

```
    {
        "mobileNo": "7056319981",
        "password": "Clickme@007"
    }
```

* Response

```
   CurrentAdminSession(id=11, adminId=10, uuid=ZaVLaK, localDateTime=2022-08-17T11:13:42.772910500)
   
```
 
### E-R Diagram Of Covid-19 Application
---
<img src="https://github.com/jitu7989/tall-yak-6508/blob/main/Covid_vaccination_service/src/main/resources/static/ER_diagram.png?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### Swagger UI

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/Swagger-ui.jpeg?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### Login Controller

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/Login.png?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### Admin Controller

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/Admin-Controller.jpeg?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### User Controller

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/User.png?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---

### Model Controller

---

<img src="https://github.com/shivamgarg796/Spring-work/blob/master/Images/mODELS.png?raw=true" style="max-width: 100%; display: inline-block;" data-target="animated-image.originalImage">

---
---
