# Flight Booking System: C++ Project

A small C++ project demonstrating **variable scopes** and **storage classes** through a flight booking system. The system manages flight bookings, tracks statistics, and maintains a booking history, showcasing the use of `static`, `mutable`, and `auto` in a practical application.

## Features

- **FlightBooking**: Create and cancel bookings with `static` tracking of seats and revenue.
- **Booking History**: Store and display booking details in a `static` vector for all flights.
- **Statistics**: Track active bookings, cancellations, total revenue, and average ticket price with formatted output.
- **Flexible Pricing**: Support custom ticket prices (e.g., $180.45, $270.99) with a default value ($366.89).
- **Robust Logic**: Prevent negative revenue and handle edge cases (e.g double-cancellation via `bookingID` check)

## Variable Scopes and Storage Classes
#### Variable Scopes:

-  `auto`: Used in `demonstrateAuto()` for string concatenation and `cancelFlight()` for vector iterators.
-  Class scope: Private members like `ticketPrice` and `passengerName`.
-  `static` scope: Shared `bookings`, `totalRevenue`, and `totalBookings` across all instances.

#### Storage Classes:

-  `static`: `bookings`, `totalBookings`, `totalCancellations`, `totalRevenue` for class-wide data.
-  `mutable`: `bookingID` allows modification in `const` methods like `cancelFlight()`.
-  Automatic: Local variables in methods like `flightInfo` in demonstrateAuto().

#### Additional Techniques:
-  Use of `<iomanip>` for formatted output (e.g $240.83 for average ticket price) and `const` correctness for read-only methods.

## Purpose
Developed as part of my C++ learning journey to demonstrate the use of variable scopes and storage classes. This project showcases my ability to design a simple system using `static` members, `mutable` variables, and `auto` type deduction, building on projects like `SchoolSystem`, `BankSystem`.

## How to Run
```bash
g++ src/mainFlightBookingReviewEx.cpp src/fns_FlightBookingReviewEx.cpp -I include -o flight
./flight
```
## Sample Output

### Booking Flights
```
Flight Booked for Rodrigo Casio on Flight001
Booking ID: 1
Total of flight ticket: $180.45

Flight Booked for John Mayer on Flight002
Booking ID: 2
Total of flight ticket: $270.99

Flight Booked for Margaret Wall on Flight003
Booking ID: 3
Total of flight ticket: $189.99

Flight Booked for LaMello Ball on Flight004
Booking ID: 4
Total of flight ticket: $250.23

Flight Booked for Marco Polo on Flight005
Booking ID: 5
Total of flight ticket: $366.89

Flight Booked for Kyrie Irving on Flight006
Booking ID: 6
Total of flight ticket: $366.89
```
### Cancelling a Flight
```
Flight Flight001 for Rodrigo Casio has been canceled successfully
```
### Booking History
```
- Booking ID: 2 | Flight002 | John Mayer
- Booking ID: 3 | Flight003 | Margaret Wall
- Booking ID: 4 | Flight004 | LaMello Ball
- Booking ID: 5 | Flight005 | Marco Polo
- Booking ID: 6 | Flight006 | Kyrie Irving
```

### Statistics 
```
Bookings active: 5
Bookings canceled: 1
Total revenue: $1444.99
Average ticket price: $240.83
```


## Author
Rodrigo Casio ([View my Github profile](https://github.com/rodrigcasio))
