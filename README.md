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
Airports:
<img width="820" height="348" alt="image" src="https://github.com/user-attachments/assets/2ea8df2e-2d25-473f-b7e5-43eac56d5542" />
Terminal:
<img width="813" height="273" alt="image" src="https://github.com/user-attachments/assets/45c82b36-396e-421d-8c0d-4c96ebcefb6a" />
Terminal Airline Assignment:
<img width="814" height="366" alt="image" src="https://github.com/user-attachments/assets/0dce80d7-b893-4379-986a-ff7ee0ecbee8" />
Airline:
<img width="809" height="245" alt="image" src="https://github.com/user-attachments/assets/cce28f51-08a6-4229-81f1-5ee675da962c" />
Employee:
<img width="819" height="588" alt="image" src="https://github.com/user-attachments/assets/259f1e59-c654-4f13-a827-26c361f6fd64" />
Crew Role:
<img width="811" height="204" alt="image" src="https://github.com/user-attachments/assets/8f00840a-c41e-4b6d-8870-2ef770b44e3f" />
Flight Crew: 
<img width="813" height="322" alt="image" src="https://github.com/user-attachments/assets/f353a43b-9c6d-4dee-bc9f-ec484ae5f0f7" />
Plane:
<img width="811" height="367" alt="image" src="https://github.com/user-attachments/assets/8ca1bb69-7913-40b8-a84f-192006bee3fb" />
Route:
<img width="809" height="359" alt="image" src="https://github.com/user-attachments/assets/f8e6a8a4-eb72-4324-8d0b-17a7a881a23f" />
Luggage:
<img width="807" height="376" alt="image" src="https://github.com/user-attachments/assets/139a76c1-7a60-490e-bdbd-e36de06117ab" />
Passenger:
<img width="811" height="267" alt="image" src="https://github.com/user-attachments/assets/70a03741-28e1-4bde-99b6-e24bc20bf9c2" />
Loyalty Tier:
<img width="811" height="224" alt="image" src="https://github.com/user-attachments/assets/3bc75e87-37f7-4804-8365-addfc82a8be3" />
Loyalty Account:
<img width="813" height="547" alt="image" src="https://github.com/user-attachments/assets/749a1c10-8776-4e7f-82c5-9461153c5f5c" />
Tickets:
<img width="813" height="517" alt="image" src="https://github.com/user-attachments/assets/3a654a9c-86d4-4498-ac43-603cb0977184" />
Flight:
<img width="809" height="672" alt="image" src="https://github.com/user-attachments/assets/4225cdb5-cc3e-4139-998b-53dafb414871" />


# Queries
1. Query 1: Lists out all possible roles for an employee and calculates the average salary for each respective role.

<img width="397" height="455" alt="image" src="https://github.com/user-attachments/assets/3891ba25-dc45-4bb6-a1f4-d2194a8ab152" />

This query will provide airlines necessary data in order to manage salary and uphold industry standards. The average salary for an employee role at an airline could be compared to the national average to see where a company stands financially. This data could also be compared to other years in order to identify trends in payments. This could also help with budgeting and managing expenses.

2. Query 2: Lists out how many pilots and copilots are employed by each airline company.
   
<img width="559" height="415" alt="image" src="https://github.com/user-attachments/assets/2b6777f5-725d-40dc-9d9a-e62fca4e6f69" />

This query provides valuable data about an airline’s staff and will help them make certain staffing decisions. Pilots and copilots are essential in flight operations and need to be balanced for the size of an airline. Understaffing will limit how many flights a company can operate, which would lead to a loss in revenue, while overstaffing would lead to unnecessary costs, especially with high-salary employees like pilots and copilots. An airline company needs to avoid both of these issues.

3. Query 3: Outputs the number of passengers that boarded a flight with no luggage.
   
<img width="683" height="707" alt="image" src="https://github.com/user-attachments/assets/68e69c87-203b-441b-8596-8426ad6c119f" />

This is important for airlines to know, as it gives data on travel habits and preferences. It will also allow companies to manage cabin space and baggage handling and fees.

4. Query 4: Outputs the number of flights for an airline that does not have a specific terminal at an airport.

<img width="621" height="433" alt="image" src="https://github.com/user-attachments/assets/1a77cd0b-88aa-4d1e-8af1-303834c8edb9" />

Some airports have airlines that have a specific terminal (such as the Delta typically), whereas other airline companies are not contracted and will go to the terminal decided by an airline. The data from this query will be helpful to both airline companies and airports. Airports will be able to see how many flights an airline has and distribute them to their terminals accordingly. This will help in the distribution of all flights to avoid overcrowding and controlling staffing and foot traffic. As for airlines, they can use this data to request specific terminals and enhance performance.

5. Query 5: Outputs the name of the airline, and the percentage of how full a flight is.
   
<img width="833" height="709" alt="image" src="https://github.com/user-attachments/assets/578e5af9-1229-4df1-852b-2382db7f5eda" />

Aircrafts only have a certain amount of seats and have a max capacity, and this data allows airlines to see how full a flight is in order to manage that. Knowing the occupancy rate is important for managers to know and understand to implement efficiency measures. This data gives insight on flight demand, seat pricing, scheduling, and more. If a flight is over 100%, then it is overbooked. This would mean there are errors with an airline's operations and they need to be more efficient.

6. Query 6: Outputs all of the flights that left a certain airport on a specific month in order to check where a luggage bag may have gone.

<img width="437" height="514" alt="image" src="https://github.com/user-attachments/assets/4ab25c1d-72b2-45ef-93ff-27d714ee873d" />

In order to find lost luggage, airlines can use data from this query to track down lost luggage and investigate bags. This will help operations run smoothly and increase customer satisfaction when luggage issues occur.

7. Query 7: Lists all airlines and the number of flights they have handled in the past 3 months

<img width="606" height="555" alt="image" src="https://github.com/user-attachments/assets/26d9c325-1a57-4104-b58e-e0c19c88bec8" />

This query provides invaluable data for an airline company. It will allow airlines and airports to monitor performance over a period of three months. This data can be analyzed in order to view spikes in flight activity, which will affect decision making regarding staffing, price, sales, etc. This information will also help an airline see its success and create visualizations about their activity. If archived, this data will be useful in the future to create predictions based on past and current flight numbers.

8.Query 8: Outputs the flight crew that has the most combined salary. This flight crew is made up of several employees.

<img width="670" height="543" alt="image" src="https://github.com/user-attachments/assets/522df7a9-5a07-45cd-9a25-c1ef51118d25" />

Airline companies need to know which employee teams have the highest salary in order to manage budget and payroll. High-salary teams may be more experienced, and could be put on longer/harder flights. This could also be used for training decisions, where an experienced, highly-paid team could teach others.

9. Query 9: Lists out all of the customers in the Platinum tier that have more than the average amount of points in that tier.
    
<img width="794" height="698" alt="image" src="https://github.com/user-attachments/assets/021da2d6-6e38-4445-8d2d-23bf725a8fe9" />

Loyalty rewards programs are a great way for customer retention and acquisition. This information will be valuable for the marketing department of an airline. This data can test the effectiveness of the loyalty program as a whole. Airlines can also use this data for targeted discounts and ads and identify their most loyal customers.

10. Query 10: Outputs the name of the terminal that has had the most ticket sales of all time.
    
<img width="838" height="568" alt="image" src="https://github.com/user-attachments/assets/f828e560-71b8-459f-8ea6-7dd0bdf3acd1" />

This query will help airline companies identify the busiest terminals at an airport. With this data, companies will be able to identify the busiest terminals and use resources accordingly. Extra staff may be placed and busy terminals and foot traffic control will be considered.


# Database Information
Name of the database: ns_F25MIST4610_15058_Group3
Call Functions: call tp_q#(). use this format to call our functions, changing the number at the end respectively.


