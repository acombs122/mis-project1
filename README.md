# mis-project1
# Team Members
1. Aidan Combs
2. Joey Maitran
3. Praneet Venigalla
4. Cameron White
5. Mariam Zaman
# Problem Description:
Our project models an operational database for the internal managerial workings of a system that coordinates flights, passengers, luggage, routes, and other aspects for multiple airlines. The core entity in our model is the Flight entity, which serves as the link between routes, planes, tickets, terminals, and other related entities. Each flight represents an instance of an aircraft journey, complete with flight crew staffing information, passenger and luggage lists, and the tickets issued for the flight. The system supports the storage and reporting of day-to-day operations data for airlines, allowing them to keep track of staffing, ticketing, and luggage management in one place.

# Data Model Overview
This data model is composed of fifteen entities, spanning various points of an airline’s operations.

The data model begins with the airport, terminal, terminal_airline_assignment, and airline entities. This database can track flights for airlines at a variety of different airports. Airports can have many terminals, hence why airports have a 1:M relationship with terminals. Furthermore, since airlines can operate out of many terminals, and terminals can house flights for many different airlines, there is an associative entity (terminal_airline_assignment) that is created.

Outside of this, the data model keeps track of staffing information in the form of employee, flight crew, and crew role information. Employees can hold a variety of different positions at the airline, and can be a part of many different flight crews. There can also be many employees in the same crew role, and many flight crews that have multiple employees occupying the same role. All of this is represented in the 1:M relationships between employees and flight crew, crew role and flight crew, and crew role and employees.

The data model also keeps track of relevant passenger information in luggage, ticket, passenger, loyalty account, and loyalty tier entities. This data model links passengers to their loyalty accounts, allowing airlines to track the status of their frequent fliers quite easily. Additionally, the model links tickets, luggage, and passengers, enabling airlines to ensure that passengers receive their luggage at their final destination in association with their ticket. The model accounts for situations like passengers booking multiple tickets and bringing multiple articles of baggage on a given trip, giving this model wide applicability.

Airline operations are maintained through the route and flight entities. Airlines operate different routes, and each of these routes may have many flights that operate on it on a given day. Furthermore, a terminal can operate many flights at a given time, hence why terminals and flights have a 1:M relationship.

Overall, the various entities and attributes that the data model captures provide an overarching view of the inner workings of an airline and its day-to-day operations to support efficient and effective managers.
<img width="1373" height="970" alt="final final png airline" src="https://github.com/user-attachments/assets/75db4623-e339-4939-9dd3-61025a8e2e82" />


# Data Dictionary
<img width="1036" height="434" alt="image" src="https://github.com/user-attachments/assets/d281a3f6-0f77-404e-ae18-f7ce7329cbc8" />
<img width="1044" height="386" alt="image" src="https://github.com/user-attachments/assets/23cf58b6-a096-4a4e-95cd-bb28bfcccb5d" />
<img width="1040" height="360" alt="image" src="https://github.com/user-attachments/assets/ed4cf168-1134-4a60-806b-2aed69a4df59" />
<img width="1034" height="324" alt="image" src="https://github.com/user-attachments/assets/e8c3e73e-414a-4c60-a67a-9294ff07cc58" />
<img width="1046" height="650" alt="image" src="https://github.com/user-attachments/assets/05425cd2-353b-4af3-b556-fd497910f31d" />
<img width="1044" height="478" alt="image" src="https://github.com/user-attachments/assets/e2b985a5-6c3e-4586-a8d9-574c2a23ed8f" />
<img width="1046" height="464" alt="image" src="https://github.com/user-attachments/assets/36732257-a44e-4f6a-9f32-e4ba94bb2ab4" />
<img width="1028" height="374" alt="image" src="https://github.com/user-attachments/assets/51167a16-d88e-440f-abf0-68654150b32d" />
<img width="1042" height="480" alt="image" src="https://github.com/user-attachments/assets/3371191a-9f0a-471f-9a4d-54ac070d1625" />
<img width="1040" height="346" alt="image" src="https://github.com/user-attachments/assets/a10a0857-0acc-4efd-8d48-42d23526ff05" />
<img width="1036" height="258" alt="image" src="https://github.com/user-attachments/assets/a349fa35-d5ea-4000-9ce1-b1c313d0735d" />
<img width="1040" height="296" alt="image" src="https://github.com/user-attachments/assets/26f10831-48d1-4fc5-aca7-c6345e10830e" />
<img width="1036" height="688" alt="image" src="https://github.com/user-attachments/assets/1d841499-0963-4599-8135-940489f0fc6f" />
<img width="1038" height="664" alt="image" src="https://github.com/user-attachments/assets/fb8bca8e-f6b8-481e-8374-743b02d8e801" />
<img width="1034" height="832" alt="image" src="https://github.com/user-attachments/assets/b60621af-c586-41ae-8982-b02eb797179f" />


# Queries










