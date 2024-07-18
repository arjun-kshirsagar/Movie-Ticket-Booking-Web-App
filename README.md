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