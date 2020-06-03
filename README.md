# GO BARBER 2.0

New Go Barber app version created during Rocketseat Bootcamp.

# Features

## Password recovery

**RF**

 - User must recover his password using his email;
 - User must receive an email with password recovery instructions;
 - User must be able to reset his password;

**RNF**

- Use Mailtrap to test mailing in dev environment
- Use Amazon SES for production email service
- Email service should ran in background

**RN**

- Password recovery link on the email must expire in 2 hours;
- User must confirm password when resetting the password;

## Profile update

**RF**

- User should be able to update his email, password and name;

**RN**

- User can't change his e-mail to an existing e-mail in the application;
- To update password, User must inform the old password;
- To update password, User must confirm the new password;

## Provider panel

**RF**

- User should be able to list his appointments of a specific day;
- Provider should receive a notification when a new appointment is booked;
- Provide should be able to view unread notifications;


**RNF**

- Provider appointments should be stored in cache;
- Provider notifications should be stored in `MongoDB`;
- Provider notifications should be sent in realtime, using `Socket.io`;


**RN**

- Notification should a read and unread status so the provider can use it;


## Appointment scheduling

**RF**

- User should be able to list all registered providers;
- User should be able to list the days of the month with at least 1 appointment available from a provider;
- User should be able to list available appointments in a single day from a single provider;
- User should ble able to book a new appointment with a provider;


**RNF**

- Provider list should be stored in app´s cache;

**RN**

- Each appointment should have exactly 1 hour;
- Appointments should be available starting from 8am to 5pm. (First at 8am, last at 5pm);
- User should not be able to book an appointment in the same time of a current existing one;
- User should not be able to book an appointment in the past;
- User should not be able to book appointments from himself as a provider;


## Techs

- NodeJS
- Typescript
- Express
- TypeORM
- Postgres
