#Event ticket booking system

A simple Java-based system where users can book tickets for events like concerts, sports matches, or theatre shows. Admin manages events, tickets, and seat availability.


Key Features

1)User Features:
 Register/Login.
 View available events.
 Book tickets (select seats, category: VIP/Normal).
 Cancel tickets.
 View booking history.
 
2)Admin Features:
 Add/Edit/Delete events.
 Set total seats & pricing.
 View all bookings.
 
3)System Features
 Seat availability check.
 Prevent double-booking.
 Show booking confirmation.
 
4)OOP Concepts Used

Class & Object → Event, User, Ticket, Admin.
Inheritance → User and Admin inherit from Person.
Polymorphism → bookTicket() behaves differently for Normal vs VIP ticket booking.
Encapsulation → Private data like password, booking ID secured with getters/setters.

UML diagram
                  ┌────────────────────────────┐
                  │        Person              │   
                  ├────────────────────────────┤
                  │  name : String            │
                  │  email : String           │
                  ├────────────────────────────┤
                  │ + showDetails() : void     │   
                  └─────────────▲──────────────┘
                                │
           ┌────────────────────┴───────────────────┐
           │                                        │
┌──────────────────────────┐            ┌───────────────────────────┐
│         User             │            │          Admin            │
├──────────────────────────┤            ├───────────────────────────┤
│ userId : int             │            │   adminId : int           │
├──────────────────────────┤            ├───────────────────────────┤
│ + bookTicket(e: Event)   │            │ + addEvent(e: Event)      │
│ + cancelTicket(id: int)  │            │ + removeEvent(id: int)    │
│ + showDetails()          │            │ + showDetails()           │
└───────────┬──────────────┘            └─────────────┬─────────────┘
            │                                         │
            │                                         │ 
            │                                         │
            ▼                                         ▼
┌──────────────────────────┐            ┌───────────────────────────┐
│         Ticket           │            │          Event            │
├──────────────────────────┤            ├───────────────────────────┤
│   ticketId : int         │            │ - eventId : int           │
│   userId : int           │            │ - title : String          │
│   eventId : int          │            │ - totalSeats : int        │
│   seatType : String      │            │ - availableSeats : int    │
│                          │            │ - ticketPrice : double    │
├──────────────────────────┤            ├───────────────────────────┤
│ + getTicketDetails()     │            │ + getAvailableSeats()     │
│                          │            │ + setAvailableSeats(int)  │ (encapsulation)
│                          │            │ + bookSeat()              │
└──────────────────────────┘            └───────────────────────────┘


