# Flight Booking System (C++)

This is a small C++ project I made to practice using variable scopes, storage classes, and basic C++ programming. The program simulates a simple flight booking system where you can book and cancel flights, see booking history, and view some statistics.

## Features

- **FlightBooking**: Create and cancel bookings with `static` tracking of seats and revenue.
- **Booking History**: Store and display booking details in a `static` vector for all flights.
- **Statistics**: Track active bookings, cancellations, total revenue, and average ticket price with formatted output.
- **Flexible Pricing**: Support custom ticket prices (e.g., $180.45, $270.99) with a default value ($366.89).
- **Robust Logic**: Prevent negative revenue and handle edge cases (e.g double-cancellation via `bookingID` check)

## Storage Classes and Variable Scopes

- **static**: Used for things that should be shared by all bookings, like the total number of bookings, cancellations, and total revenue. This means every booking can update these numbers.
- **mutable**: Lets us change some values (like `bookingID`) even in functions that are supposed to be "read-only" (const methods).
- **auto**: Makes the code a bit easier to write by letting C++ figure out the type for us, especially when working with things like iterators or strings.
- **Local variables**: Regular variables that only exist inside a function, like when we calculate the average ticket price.

These helped me learn how to organize data and logic in a way that makes sense for a small project.

## Purpose

I made this project to get better at using things like `static` variables, `mutable` variables, and `auto` in C++. It helped me understand how to organize code for a small system and how to use different storage classes and variable scopes.

## How to Run
This project uses **CMake** build system generator for easy, cross-platform compilation. Follow these steps from the root directory of the project `FlightBookingEx/`

1. **Ensure CMake is installed:**
- Make sure you have CMake (version 3.1- or higher please) and a C++ compiler (g++ or clang++) installed on your system.

2. **Generate the build system (configure):**
- Create a separated directory for the build files  and run CMake inside it. Keeping source files clean

```bash
mkdir build
cd build
cmake ..
```

3. **Build:**
- Use generated build system (`make` on Unix-like systems) to compile the executable.

```bash 
make
```

4. **Run the program:**
- The executable (FlightBookingEx) will be placed inside the `build` directory.

```bash 
./FlightBookingEx
```

**IMPORTANT: Note for windows users:**

- Windows developers have two ways to build the project using CMake.
  - **Command line (MSYS2/Cygwin):** If you use an environment like **MSYS2** or **WLS** (Windows Subsystem for Linux), you can follow the **Standard Build** steps above exactly.
  - **Visual Studio:** CMake can generate a Visual Studio solution. Run CMake from your `developer command prompt`, specify the generator:

```bash 
cmake .. -G "Visual Studio 17 2022"
```

Then, open the generated `.sln` file and build within Visual Studio IDE.

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

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)
