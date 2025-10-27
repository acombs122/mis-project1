# mis-project1

# Problem Description:
Our project models an operational database for the internal managerial workings of a system that coordinates flights, passengers, luggage, routes, and other aspects for multiple airlines. The core entity in our model is the Flight entity, which serves as the link between routes, planes, tickets, terminals, and other related entities. Each flight represents an instance of an aircraft journey, complete with flight crew staffing information, passenger and luggage lists, and the tickets issued for the flight. The system supports the storage and reporting of day-to-day operations data for airlines, allowing them to keep track of staffing, ticketing, and luggage management in one place.

# Data Model Overview
This data model is composed of fifteen entities, spanning various points of an airline’s operations.

The data model begins with the airport, terminal, terminal_airline_assignment, and airline entities. This database can track flights for airlines at a variety of different airports. Airports can have many terminals, hence why airports have a 1:M relationship with terminals. Furthermore, since airlines can operate out of many terminals, and terminals can house flights for many different airlines, there is an associative entity (terminal_airline_assignment) that is created.

Outside of this, the data model keeps track of staffing information in the form of employee, flight crew, and crew role information. Employees can hold a variety of different positions at the airline, and can be a part of many different flight crews. There can also be many employees in the same crew role, and many flight crews that have multiple employees occupying the same role. All of this is represented in the 1:M relationships between employees and flight crew, crew role and flight crew, and crew role and employees.

The data model also keeps track of relevant passenger information in luggage, ticket, passenger, loyalty account, and loyalty tier entities. This data model links passengers to their loyalty accounts, allowing airlines to track the status of their frequent fliers quite easily. Additionally, the model links tickets, luggage, and passengers, enabling airlines to ensure that passengers receive their luggage at their final destination in association with their ticket. The model accounts for situations like passengers booking multiple tickets and bringing multiple articles of baggage on a given trip, giving this model wide applicability.

Airline operations are maintained through the route and flight entities. Airlines operate different routes, and each of these routes may have many flights that operate on it on a given day. Furthermore, a terminal can operate many flights at a given time, hence why terminals and flights have a 1:M relationship.

Overall, the various entities and attributes that the data model captures provide an overarching view of the inner workings of an airline and its day-to-day operations to support efficient and effective managers.

# Data Dictionary

# Queries
