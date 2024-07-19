# Movie-Ticket-Booking-WebApp

## Bug 1: Moving the Seat Booking Matrix to the Middle.

### Initial Commit
![Initial Bug](./project/assests/Initial%20Bug.png)

### Final Output
![Final Output](./project/assests/Final%20Output.png)

## Bug 2: Added Hyperlinks to Home & BookMyShow Component

![Hyperlinks directing to Home Page](./project/assests/HyperLinks.gif)

## Bug 3: Role-Based Access Control
### Problem:
Previously, users were able to access the /admin and /partner panels regardless of their roles. Similarly, partners could access the /admin panel, leading to unauthorized access to restricted areas of the application.

### Expected Behavior
Users should only be able to access panels that correspond to their roles:

- Admins should have access to the /admin panel.
- Partners should have access to the /partner panel.
- Unauthorized users should not have access to any restricted panels and should be redirected appropriately.

### Solution:
Implemented a role-based access control system to ensure that users can only access panels for which they have the appropriate roles. Unauthorized users attempting to access restricted panels will be redirected to the Unauthorized page (/unauthorised).

### Unauthorized Page

![Unauthorized Page](./project/assests/Access%20Control.png)


## Bug 4: Booked Seats Being Considered for Booking

### Problem
When a user clicks on a seat that has already been booked, the "Pay Now" button appears, and the amount of the booked seat is included in the total price and selected seats. This should not happen, as booked seats should not be available for selection.

![Rebooking Bug](./project/assests/Rebooking%20Bug.png)

### Expected Behavior
Users should only be able to book unbooked seats. Once a payment is successful, the booking details should be updated in the database, and the user should be redirected to the "/profile" page.

### Solution
To prevent booked seats from being selected and included in the total price, the onClick handler for seat selection was updated. This ensures that booked seats cannot be selected or deselected by users.

![Disabled Rebooking of the same seat](./project/assests/Disabled%20Rebooking.png)