# Collections

This week features a short set of practical exercises to get you used to working with collections.
We are only working with ArrayList and HashMap in this practical.

Close the repository and open the Student and Main classes in the `collections` package. The Student class is a
simple data structure for storing a student's name and grade. It also contains `STUDENTS_ARRAY` which consists of some
students with names and grades created using random generators. In this practical you will mostly be writing code in
the Main class, but you will also need to make some changes to the Student class.

Start by working in the `main()` method inside the Main class, adding your code after the comment for the step you are
currently completing. You may want to refer to the lecture material to learn how to complete some of these steps.

## Step 1: Declare a variable named ArrayList

Self-explanatory. If you are not yet used to the syntax for generics, now is a good time to learn. Remember to both
declare the variable and initialise it to a new ArrayList, otherwise the subsequent code will break.

## Step 2: Add the students in Student.STUDENTS_ARRAY to your ArrayList

Student.STUDENTS_ARRAY is an array of Student objects. Add all of the students in this array to your ArrayList.
There are multiple ways of doing this; the most obvious is to loop through the array and `add()` every item to the
ArrayList, but there are also methods in the JDK that will handle this for you. Either approach is fine.

## Step 3: Create a displayStudents() method

Create a new method in the Main class called displayStudents. It should take an ArrayList<Student> and print out a
list of students, showing the student's name and grade, one student per line.

Hint: To make this method more flexible, make it take a List<Student> or even a Collection<Student> instead.

## Step 4: Sort the ArrayList into alphabetical order, then display the students

In this step, you will need to make the Student class comparable, then add a compareTo method to facilitate alphabetical
ordering of the list of students. Then you can simply use the Collections.sort() method to sort the array. Then display
the list of students with your new displayStudents() method.

Also experiment with sorting by ascending and descending order of grades.

## Step 5: Create a HashMap<String, Student> and add the students to it

Add all the students to a new HashMap. While lists are great for data that needs to be iterated over, or have new values
inserted at the end, they are inefficient to search. While the list is in unsorted order, if we want to find a
particular student by their name, we need to iterate through the entire list in order to do it. If we sort the list
first, we can do a binary search and find the student in log(n) comparisons, which is much faster. However, a HashMap
will allow us to find the student in constant time, which is important as data sets become larger.

Once again, the easiest way is to loop over the ArrayList and add all the students, but there are other ways that only
involve a single method call.

## Step 6: Use the HashMap and set Joshua's grade to 95, then display the students

Now that we have a HashMap, looking u an individual student object by its name is quick and easy. An error was found
when checking Joshua's second assignment. Find the student named Joshua and set his grade to 95, using the HashMap to
make this process fast.

## Step 7: Add JavaDoc-style comments and generate JavaDoc for the project.

Documentation is important for any project. When working with others, you want to document what your code does
so that they can use your classes and methods as they were designed, and minimise the likelihood of integration errors.
In addition, properly documented source code will help you use your own methods, especially after coming back to old
code you haven't touched in a while. Using the 'Documentation' section of the lecture as a reference, document the
Student class and its public methods with JavaDoc-style comments. Also document the displayStudents() method in Main
that you created (and make it public if it is not already).

Once you have done this, generate JavaDoc for your project. In IntelliJ go to Tools -> Generate JavaDoc. You will need
to specify the directory for the JavaDoc documentation to be generated in- create a directory called 'doc' inside your
project folder for this.
