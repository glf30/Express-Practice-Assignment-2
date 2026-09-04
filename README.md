# Express-Practice-Assignment-2

Congratulations on sharpening your API building skills! You will now work as a developer for an event coordinatior office in NYC. Residents frequently ask what events are happening in different parts of the city, what type of events they are, and whether they are free or paid. The city wants an API that allows flexible searching based on the URL and query parameters.

For this assignment, you will work with the following data:

```js
const events = [
  {
    id: 1,
    name: "Central Park Summer Concert",
    borough: "manhattan",
    type: "music",
    free: true,
    day: "saturday"
  },
  {
    id: 2,
    name: "Brooklyn Night Market",
    borough: "brooklyn",
    type: "food",
    free: true,
    day: "friday"
  },
  {
    id: 3,
    name: "Queens Food & Culture Festival",
    borough: "queens",
    type: "food",
    free: false,
    day: "sunday"
  },
  {
    id: 4,
    name: "Bronx Outdoor Movie Night",
    borough: "bronx",
    type: "movie",
    free: true,
    day: "friday"
  },
  {
    id: 5,
    name: "Staten Island Art Walk",
    borough: "staten island",
    type: "art",
    free: false,
    day: "saturday"
  },
  {
    id: 6,
    name: "Downtown Jazz Showcase",
    borough: "manhattan",
    type: "music",
    free: false,
    day: "thursday"
  }
];
```

## Routes

`GET /`  
  Returns the full list of events.

- `GET /borough/:boroughName`  
  Returns all events for the given borough . If no events are found, respond with a 404 status and a message indicating no events were found for that borough.

- `GET /type/:eventType`  
  Returns all events that match the given event type.

- `GET /events/:id`  
  Returns a single event matching the provided numeric `id`. If the event does not exist, respond with a 404 status and an appropriate message.

- `GET /search`  
  Allows filtering events using any combination of query parameters:
  - `type` (event type)
  - `free` (`true` or `false`)
  - `day` (day of the week)

  If no events match the provided search criteria, respond with a 404 status and a message indicating no results were found.

- Any unknown route should return a 404 status with a `"Route not found"` message.
