# Hackathon Sequence Diagram
```mermaid
sequenceDiagram

    participant User as User
    participant GUI as GUI
    participant Request as Request
    
    User->>+GUI: User activates GUI. 
    activate GUI
    GUI->>+Request: makeRequest() makes API to gather data.
    activate Request
    Request-->>-GUI: Returns data to GUI
    GUI->>GUI: Parse Data for Upcoming Assignments and display to User
    GUI-->>User: GUI Displays Upcoming Assignments to User
    User->>GUI: Press Assignments
    GUI->>GUI: Parse Data for all Assignment Events and display to User
    GUI-->>User: Display Assignments
    User->>GUI: Press Lectures
    GUI->>GUI: Parse Data for all Lecture Events and display to User
    GUI-->>User: Display Lectures
    User->>GUI: Press Labs
    GUI->>GUI: Parse Data for all Lab Events and display to User
    GUI-->>User: Display Labs
    User->>GUI: Press Sprints
    GUI->>GUI: Parse Data for all Sprint Events and display to User
    GUI-->>User: Display Sprints
    User->>GUI: Press BREAK
    GUI->>GUI: Parse Data for all Break Event and display to User
    GUI-->>User: Display Break Event
    User->>GUI: Press Upcoming
    GUI->>GUI: Parse Data for Upcoming Events and display to User
    GUI-->>User: Display Upcoming Events
    User->>GUI: Close button
    GUI-->>-User: Gui closes
