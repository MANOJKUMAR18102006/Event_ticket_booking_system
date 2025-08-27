#Event ticket booking system

A simple Java-based system where users can book tickets for events like concerts, sports matches, or theatre shows. Admin manages events, tickets, and seat availability.

Key Features

1)User Features
 Register/Login.
 View available events.
2)Book tickets (select seats, category: VIP/Normal).
 Cancel tickets.
 View booking history.
3)Admin Features
 Add/Edit/Delete events.
 Set total seats & pricing.
 View all bookings.
4)System Features
 Seat availability check.
 Prevent double-booking.
 Show booking confirmation.
5)OOP Concepts Used

Class & Object → Event, User, Ticket, Admin.

Inheritance → User and Admin inherit from Person.

Polymorphism → bookTicket() behaves differently for Normal vs VIP ticket booking.

Encapsulation → Private data like password, booking ID secured with getters/setters.

Abstraction → Abstract class Person defines common properties (name, email).
