# Ex.No: 10  Logic Programming –  Simple queries from facts and rules                                                                           
### REGISTER NUMBER : 2122230060045
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
food(apple).
food(vegetable).
eats(bill,peanuts).
alive(bill).
eats(sue,X):-eats(bill,X).
eats(bill).
```
### Output:
![316232180-0804bca9-ce70-459f-822b-3de4a4c090bd](https://github.com/user-attachments/assets/4a7adaed-5ff1-43fe-afb9-9c70890d289e)

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
          course(X,dept(havefun)).
course(bk301,dept(havefun)).
```
### Output:
![316232216-318f38c1-c5b8-40b2-b523-f55bd74ba528](https://github.com/user-attachments/assets/318b95a9-5423-40ca-8ab4-50d2e3fa5e9e)

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
criminal(X):-
	american(X),
	weapon(Y),
	hostile(Z),
	sells(X,Y,Z).
weapon(Y):-
    missile(Y).
hostile(Z):-
    enemy(Z,X).
sells(west,Y,nano):-
    missile(Y),
    owns(nano,Y).
missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```
### Output:
![316232243-aa255296-7016-48c3-bf05-336df6bcc1d0](https://github.com/user-attachments/assets/323755fc-2966-4ea0-9ac0-d6ce9f39e898)
### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
