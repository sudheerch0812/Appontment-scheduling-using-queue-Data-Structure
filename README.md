# Appontment-scheduling-using-queue-Data-Structure
The provided C code offers a simple framework for an appointment scheduling system, yet it presents certain challenges and shortcomings. While it allows users to add and display appointments, it lacks a comprehensive mechanism for error handling, input validation, and data persistence. 

#include <stdio.h>
#include <stdlib.h›
/ Define the structure for an appointment
- struct Appointment {
char name[50]; char date[20];| char time[20];
struct Appointment* next;
};
// Define a structure for the queue
struct Queue {

struct Appointment* front;

struct Appointment* rear;
 };
// Function to create a new appointment
* struct Appointment* createAppointment) {
struct Appointment* newAppointment = (struct Appointment*)malloc(sizeof
(struct Appointment));
if (newAppointment == NULL) {
printf("Memory allocation failed. \n");
exit (1);

}
printf ("Enter Name: ");
scanf ("%S", newAppointment-> name);
printf("Enter Date (MM/DD/YYYY): ");
scanf ("%s", newAppointment-› date);
printf("Enter Time: ");
scanf ("%s", newAppointment->time);
newAppointment ->next = NULL;
return newAppointment;
}
// Function to initialize a queue
struct Queue* createQueue() {
struct queue* queue = (struct Queue*)malloc(sizeof(struct Queue));
if (queue == NULL) {
printf ("Memory allocation failed, In");
exit(1);
queue-> front = queue-›rear = NULL;
return queue;
}
// Function to enqueue an appointment
• void enqueue/struct Queue* queue, struct Appointment* newAppointment) {
 if (queue-›rear == NULL) {
 int choice;
while (1) {
printf("nAppointment Scheduling System\n");
printf ("1. Add Appointment\n");
printf("2. Display Appointments \n");
printf ("3. Exit\n");
printf ("Enter your choice: ");
scanf ("%d", &choice);
switch (choice) {
case 1: {
struct Appointment* newAppointment = createAppointment();
enqueue(appointmentQueue, newAppointment);
printf ("Appointment added to the queue. In");
break;
case 2: {
break;
displayAppointments (appointmentQueue);
}
case 3: 1
printf("Exiting the program. In");
exit (0);
}
default:
}
default:
print ("Invalid choice, Please try again. In*);
}
}
return 0;
}
