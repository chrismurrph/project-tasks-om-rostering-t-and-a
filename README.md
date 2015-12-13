### project-tasks-om-rostering-t-and-a

# Methodology/steps to writing a Rostering and Time and Attendance application 

1. ERD from TH

2. Incorporate: 
  * Location 
  * Different roster slots (obviously a library has different shifts than TH) 
  * Roles 

3. Put TH test data in a DataScript database. (Memory only, CLJS)

4. Augment the ERD to include Time and Attendance and budget. (We will need to do analysis here).

5. Give a name to every screen we can think of. (Actually using the TH rostering program will help).

6. Name the DevCards that these screens are composed of.

7. Views for all DevCards (do in a templating system like hiccup so can bring test data in)

8. Datascript query for each DevCard so it can be populated

9. Name and categorise all the Om-Next components that will be required. They will be categorised as pure or application. Describe their read and mutate functions, preferably in pull syntax.

10. The UI is a graph and we have the names of all the components, so lets draw the graph.

11. We have queries, UI graph and ERD. Do thought experiments. Does it all fit? Need changed?

12. Write down 20 typical interactions of the various roles.

13. Since we have the data too, lets think up and write 20 tests. These tests are for fully going into and back out from the application, having mutated the (whole of the graph of) data in some way.

14. Write Om-Next components to make these tests pass. Note that no UI is required to do this.

15. If any of the named components have not yet been written then we need to write more tests to ensure they are, till get 100% coverage.

16. Views from step 7 to become Om-Next component render functions.

17. The DevCards can now be backed by actual components. Note that these are still 'low level' components and an extra 'feeder' query will be required for them all. This is the query we wrote at step 8.

18. Get high-level layout-management Om-Next components to compose together with nothing in them but named panels. So the skeleton of the application has been created but can't be navigated.

19. Have buttons and tabs so that navigation can be made to work.

20. Put queries on all of these high level components.

21. Put rest of the components in and we should have a working Client-side only application.

22. Setup Datomic Server same as the DataScript one.

23. Get working across the wire.

24. Populate with more realistic data - test database

25. UAC

26. Create another DB which will be the LIVE one. Depending on your username you go into a different database. 



