#Doctor's API

##How to Setup Project

###Proceed with the following steps to install the project:

1. Open application.properties file in src/main/resources folder, and set port number, database username, password.
2. Create database in mysql as 'patientappointments'.
3. Open the project with any supporting IDE. I created it using Intellij.
4. Let the IDE install all the dependencies.
5. Find and set main class as '\src\main\java\com\ankitnegi\doctors_api\DoctorsApiApplication.java'.
6. Project uses Lombook, JPA, Hibernate, MySQL and Spring Boot.
7. Make sure all the dependencies/libraries for the above are installed.


##How to Run
1. Click on Run.
2. Using Postman, Send respective API request.

###API Requests:-
####Patient API -
1. Adding a record: POST /patients
Example JSON body-
{
    "email": "kamlesh@gmail.com",
    "address": "rpg, dehradun",
    "name": "Kamlesh",
    "password": "8000",
    "phone_number":"4232352343"
}

2. Updating existing patient: PUT /patients
Example JSON body-
{
    "email": "email@gmail.com",
    "address": "updated adr, dehradun",
    "name": "Kamlesh Updated",
    "password": "8000updated",
    "phone_number":"4232352343"
}

3. Deleting a patient record: DELETE /patients/{email}

4. Fetching all the patient records: GET /patients


####Patient API -
1. Scheduling Appointment: POST /schedule/{email}
Example JSON body-
{
    "datetime": "2021-09-08T20:17:34.000+00:00",
    "address": "updated adr, dehradun",
    "name": "Kamlesh Updated",
    "password": "8000updated",
    "phone_number":"4232352343"
}

2. Fetch all appointments ordered by date: GET /schedule