1. A list consisting of reminders the users want to be aware of. The application must allow
   users to add reminders to a list, delete reminders from a list, and edit the reminders in
   the list.
   
    -To realize this requirement, I added to the design a class ListOfReminders with operations to add, delete, and edit reminders.
2. The application must contain a database (DB) of reminders and corresponding data.
    
    -UML representation of a database that's connected to class List and ListOfReminders so newly created reminders and lists can be saved and searched.
3. Users must be able to add reminders to a list by picking them from a hierarchical list,
   where the first level is the reminder type (e.g., Appointment), and the second level is the
   name of the actual reminder (e.g., Dentist Appointment).
   
    -I added an interface that will enable the user to choose the type from a list and create the reminder that will be added to the list reminders class.
4. Users must also be able to specify a reminder by typing its name. In this case, the
   application must look in its DB for reminders with similar names and ask the user
   whether that is the item they intended to add. If a match (or nearby match) cannot be
   found, the application must ask the user to select a reminder type for the reminder, or
   add a new one, and then save the new reminder, together with its type, in the DB.
    
    -Added a search to List class since its directly connected to the database that contains the reminders, the rest of the specifications can be implemented by the UI.
5. The reminders must be saved automatically and immediately after they are modified.
   
   -Shown through the direct connection of the database to the class ListOfReminders so that reminders can be saved after creation.
6. Users must be able to check off reminders in the list (without deleting them).
   
   -An operation created in ListOfReminders that collects all checked reminders and a bool attribute in reminders class to assign check/unchecked status.
7. Users must also be able to clear all the check-off marks in the reminder list at once.
   
   -Operation in ListOfReminders to clear all checked reminders
8. Check-off marks for the reminder list are persistent and must also be saved immediately.
   
   -Previous operations 6 and 7 are in ListOfReminders class which is directly connected to the database allowing changes to be saved.
9. The application must present the reminders grouped by type.
   
   -Reminders saved by group in the ListOfReminders will be displayed, when called, by the UI.
10. The application must support multiple reminder lists at a time (e.g., “Weekly”, “Monthly”,
    “Kid’s Reminders”). Therefore, the application must provide the users with the ability to
    create, (re)name, select, and delete reminder lists. 

      -Lists class created that has add, delete, and rename operations.
11. The application should have the option to set up reminders with day and time alert. If this
    option is selected allow option to repeat the behavior.
   
      -An interface connected to class remindes that tells if and how often there are alerts with operations to distinguish between daily, week, month, and an operation for the date and time span. 
12. Extra Credit: Option to set up reminder based on location.
   A getLocation operation in the Reminders class that is connected to a location obtaining service.
13. The User Interface (UI) must be intuitive and responsive.

      -Not considered because it does not affect the design directly.