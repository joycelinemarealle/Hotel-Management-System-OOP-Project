# Hotel-Management-System-OOP-Project

Project: Object-Oriented Development
Hotel Booking System

SUMMARY:
Developed an object-oriented Hotel Booking System in Java, incorporating input validation, room booking, check-in/check-out tracking, room cleaning management, guest services billing, loyalty program implementation, and seasonal rate adjustments


PROJECT DETAILS:
During the pandemic, when few people were traveling, a new luxury hotel opened up. With only a few visitors, they were managing to handle all their room bookings manually in a paper diary. However, as demand started to increase, they found it increasingly difficult to manage.
For this project, I worked in pairs using pair programming, and the new booking system we developed was object-oriented. 

Note: We provided a command line, text-based, menu-driven interface similar to what we had developed during our lab exercises. There was no graphical user interface developed as part of this project.

The hotel team identified a number of functional requirements, listed from highest to lowest priority in terms of their business:

FR1: Book a Room
The most basic need was to be able to book a room for a customer. The hotel had only six rooms, and a room could only be booked by a single customer at any given time. The rooms were of different types:
2 x Double Standard (charged £150 per night)
2 x Deluxe Double (charged £200 per night)
1 x Junior Suite (charged £300 per night)
1 x Grand Suite (charged £400 per night)

All the rooms could support a maximum of 2 occupants: a primary customer who made the booking and a guest. The name of the guest had to be recorded on the booking.

FR2: Check-in and Check-out
The rooms in the hotel were available for check-in from 3pm, and guests had to check out before 12 noon, leaving a 3-hour window for cleaning.
To facilitate this, the hotel needed to track when a guest arrived at the hotel for the first time and checked into their allocated room, as well as when they departed at the end of their stay and checked out.
Guests had to visit the reception desk to both check in and check out.
If a guest had not checked in by midnight on the day of the booking, the booking was automatically canceled, and the room was released for other customers.

FR3: Track Room Cleaning
Before a guest could check in, rooms had to be cleaned. The hotel tracked if individual rooms had been cleaned once a guest checked out and before a new guest could be allocated the room on check-in.
Until a room had been cleaned on a specific day, no guests could check in.

FR4: Guest Services
The hotel provided additional services for guests, including:
Breakfast (£10 per person, per day)
Room Service (a fixed price of £20 per meal, per person on request)
Laundry Service (a fixed price of £5 per item, on request)
The hotel identified any extra items that had been purchased for a given booking and produced a final bill. The bill was made up of the base room charge, plus any additional spending a customer may have made.

FR5: Customers and Loyalty
The hotel offered a loyalty program, so that repeat customers could get a discount on future stays. Once a customer had completed their stay (they had checked out of the room), for every night they had stayed, up to a maximum of 20 nights, they received a 1% discount on any future bookings.
For example, if James stayed at the hotel for 10 nights, on his next booking he received a 10% discount. If he then stayed a further 5 nights, on his next booking he received a 15% discount. Finally, if he stayed for a further 15 nights, he received the maximum discount of 20% on any of his future bookings.

FR6: Manage the Rates of Rooms
The hotel wanted the ability to manage the room rates for the different types of rooms they had.
As a stretch goal, they wanted this to be based on the season; for example, during winter a Double Standard room might cost £100 per night, but during summer months £175 per night.
In all cases, updating the price did not impact existing bookings (anyone who had already checked in, and certainly anyone who had checked out).

FR7: The Hotel is Expanding
The hotel was in the process of being extended. Once open, the extension would introduce 4 new rooms. Two of these rooms were Deluxe Double rooms, and the hotel was also introducing a new Family Room. The Family Room could sleep three occupants and had a double bed and a single bed.
The hotel wished to be able to create, update, and remove room types from the system to accommodate this expansion and any future expansions they had planned.

When adding a new room type, the hotel specified:
How many people the room could sleep (e.g., 3)
The initial price per night (e.g., £225 per night)
The name of the room type, e.g., "Family Room"
The number of rooms of this type that there were (e.g., 2)
When updating rooms, the hotel could change:

The name of the room type, and this impacted all future bookings, but not those where someone had already checked in.
The number of rooms of the type, but this was never fewer than the number of current or future bookings.
The cost per night (see FR6).
If the hotel decided to remove a room type completely, then any future bookings, where a guest had not yet checked in, were automatically canceled.

FR8: A New Hotel
The hotel hoped to expand and open a new hotel in the neighboring city. The new hotel would have 12 rooms initially, a mix of:
4 x Double Standard
4 x Deluxe Double
2 x Family Rooms
1 x Junior Suite
1 x Grand Suite

The hotel wanted the new hotel to use the same booking system, so that customers and loyalty discounts earned at the current hotel were valid in the new hotel.
The system allowed customers to pick which hotel they wished to book into. If a customer wished to change their booking to another hotel, they had to cancel their existing booking and make a new one; the hotel did not support "portable" bookings.
