# Support for Compute Intensive Events


### Calendar Scaler

The Google Calendar Scaler in DataHub, with this additional setup, functions as a dynamic resource allocator that specifically adjusts the number of spare or “hotspare” nodes available, rather than the total number of active nodes. These spares act as placeholders to accommodate sudden bursts of user logins and prevent service delays. If you are teaching a course that requires sudden surge of user logins for a short period of time then you can consider using calendar scaler.

### How It Works
**Integration with Google Calendar API:** The scaler is connected to a specific Google Calendar (in our case `datahub-scaling-events` through the Google Calendar API. This setup allows the scaler to read events scheduled within the calendar, using them to monitor upcoming computational needs.

**Event Monitoring:** The scaler checks for specific events or tags in the above mentioned Calendar. For example, there might be events labeled "Class Lecture," "Workshop," or "Assignment Deadline" that are used to signal periods when additional resources are needed.

**Hotspare Node Management:** Instead of setting a fixed number of total nodes, the scaler is configured to maintain a specified number of "hotspare" nodes—empty nodes kept on standby. These hotspares enable rapid ramp-up to handle bursts of logins without making users wait for node provisioning. For example, if 350 students are expected to log in at once for a class starting at 4:30 p.m., we can set two spares at 4:20 p.m. (based on the typical load per node) to ensure enough capacity to manage an influx of users without delays.


### Benefits

**Initial Surge:** For anticipated high-load events, like the start of a large class, the spare count is temporarily increased to handle a large number of logins in a short period (e.g., two spares could handle around 90 logins instantly).

**Usage Count:** A short spike in large count of user login may justify more spares, while a gradual ramp-up requires fewer. If fewer users log in than expected, the spare count can be quickly reduced.

In essence, this configuration allows DataHub to scale responsively based on perceived user demand.