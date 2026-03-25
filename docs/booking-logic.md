```markdown
### `checkHostReadyAvailability(propertyId, requestedDates, currentBookings)`

Checks if a property is available for a specified set of requested dates, taking into account current bookings.

#### Parameters

- `propertyId` (string): The unique identifier of the property to check for availability.
- `requestedDates` (Date[]): An array of `Date` objects representing the dates for which availability is being requested.
- `currentBookings` (Array<Object>): An array of existing booking objects. Each object must conform to the following structure:
    - `propertyId` (string): The ID of the booked property.
    - `startDate` (string | Date): The start date of the booking. Must be a format parsable by `new Date()`.
    - `endDate` (string | Date): The end date of the booking. Must be a format parsable by `new Date()`.

#### Returns

- `boolean`: `true` if the property is available for *all* `requestedDates`.

#### Throws

- `Error`: If the property is unavailable for *any* of the `requestedDates`. The error message will be: "Vector Swarm routing: Property is unavailable for selected dates."
```