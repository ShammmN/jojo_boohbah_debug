# jojo_boohbah_debug
Question 1: 
The group by does not include name in the command but only boohbah_id which means it will only aggregate by boohbah_id leaving SQL with columns that are not aggregated. I added the name column to the group by function to make the SQL aggregate it. 

Question 2: 
The columns are not being joined together using the correct table because the boohbah_stand_link table connects the stands and boohbahs so just using boohbah table and jojo_stand table to connect the boobah and stands together wont work because them having the same id doesn't mean they are connected only the boobah_stand_link table connects them. That is why I gave the boohbah_stand_link table and jojo_stand table join clauses and connected all three tables to each other. 

Question 3: 
The column name used to identify the boohbah’s name is not the same as the actual column name in the table which is why there was an error because it couldn't find that name. Checking the table I figured out the actual column name and changed the command to have the actual name. 

Question 4: 
The column names do not have an identifier table to tell which table it is retrieving the column from. I added the table that the column is supposed to be retrieved from for each column name. Since there are multiple tables being called you need to specify by using the tables alias before the column name to specify which table that column is being retrieved from. 

Question 5:
It originally compares the boobah energy levels to see which are greater than the average of each boohbah instead of checking which are greater than the overall average of all the boohbahs. That is why I removed the WHERE clause which is what is giving an average for each boohbah id. 

Question 6: 
The command is taking data from multiple rows when it is supposed to be comparing one row to another one row but instead it's one row to multiple. I added MAX to the power column to find just the largest power and compare that to the energy levels of the boobahs. 

Question 7: 
The command was not using all three tables to connect the stand name and the boohbahs which is why the boohbahs were connected to multiple stand names and it is displaying multiple stand name connections for each boohbah. I added join clauses to connect the three tables by their ids using the boohbah_stand_link table to connect both boohbah and jojo tables together by an actual link. 

Question 8: 
This command requires you to create a subquery and use the select clause to choose the column that you need to compare. When you AVG a column, you create a subquerry because you are making a new column. That is why I used a select clause in parentheses for the AVG column. 

Question 9: 
This code works but is just repeating what it is trying to do. It just makes a simple thing longer. That is why I simplified it by just having the one select and from statements. 

Question 10: 
The ON clause is not correct, it is not comparing the correct columns. It is just comparing the id columns from the tables but it needs to compare the id columns from the boohbah_stand_link table because it is the table that actually correlates them correctly. That is why I added an extra subquery specifically selecting those id columns from the boohbah_stand_link table. 
