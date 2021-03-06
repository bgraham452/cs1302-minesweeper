# CSCI 1302 - Minewseeper Project (cs1302-minesweeper)

Skeleton code for the Minesweeper project assigned to the students in Michael E. 
Cotterell's Fall 2012 CSCI 1302 class at the University of Georgia. Please read 
the entirety of this file before beginning your project.

## Academic Honesty

You implicitly agree to Academic Honesty policy as outlined in the course 
syllabus and course website (available at: http://cs.uga.edu/~mec/cs1302/).

In accordance with the notice above, I must caution you to **not** fork this
repository on GitHub if you have an account. Doing so will more than likely make
your copy of the project publicly visible. Please follow the instructions 
contained in the Resources section below in order to do your development on
<code>nike</code>.

For this project, you are allowed to share code with your group partner. Please
see the section on Pair Programming below.

## Project Description

Your goal is to develop a Minesweeper game with a graphical user interface
implemented in Swing. Instructions and specific implementation details are
presented below.

## Pair Programming

Students are required to work in groups of two for this project. Furthermore,
each group needs to engage in _pair programming_. Pair programming is an agile 
software development technique in which two programmers work together at one 
workstation. One, the _driver_, writes code while the other, the _observer_ 
(or _navigator_), reviews each line of code as it is typed in. The two 
programmers switch roles frequently.

Yes, this involves physically meeting with your partner. Not being able to
find time is NOT an excuse for not participating. If you need a place to meet
and work on the project then I suggest the 307 lab in Boyd. The iMacs are
already setup with everything you need. You login to them with your <code>nike</code>
account and all of your <code>nike</code> stuff is already there.

## Project Tasks

Before you submit your project, you need to perform the following tasks. Please
note that each task has an individual due date. This will give the graders a 
chance to review your group's progress.

 1. (10 points) Design the graphical user interface for your game using a 
    mock-up tool such as [Pencil](http://pencil.evolus.vn/). Your GUI should
    allow users to start and play a new game. The actual game board should be
    implemented in the GUI. Each coordinate should either be covered or, if
    uncovered, it should contain either a blank or a number. If the user clicks
    on a coordinate that contains a mine then all mines on the board are 
    displayed and the game is over. The user should also be given the option to
    start a new game. Initial mock-up images are due 2012-10-26 @ 11:59pm.

 2. (10 points) Design the classes for your project using a UML tool such
    as [Astah Community Edition](http://astah.net/editions/community). This
    structure can be based on the some of the classes from Project 1, but will
    need to be extended to support a graphical user interface. Make sure that
    your minesweeper game is designed to handle the recursive case. More 
    information about this will be provided below. The initial set of 
    UML diagrams is due 2012-11-02 @ 11:59pm.

 3. (30 points) Implement your classes based on the UML diagrams and GUI mock-ups
    you submitted. If you need to make modifications to that design then you must 
    submit updates to both your UML diagrams and GUI mock-ups as needed to reflect 
    the current state of development. This is due 2012-11-09 @ 11:59pm.

 4. (20 points) Create JUnit tests for classes and methods that can be tested.
    This is due 2012-11-09 @ 11:59pm.

 5. (10 points) Ensure that your code is properly documented using inline comments as 
    necessary. In general, you should describe in regular terms what it is the
    code that you are writing is doing. A small example of such comments can be
    seen in the <code>createAndShowGUI</code> method in the  <code>Calculator</code>
    class. Please note that you do not need to write JavaDoc comments for the 
    methods that implement methods in the <code>Math</code> interface as they 
    will inherit the comments from the interface. However, if you create any new
    methods or classes then they will need to be properly documented using
    JavaDoc comments and tags. This is due 2012-11-09 @ 11:59pm.

 6. (20 points) Version Control. You will be required to use <code>git</code> for
    this project. A portion of your grade will be determined based on you and
    your partner's <code>git log</code>. Please follow the directions outlined
    in the resources section carefully in order to make sure and your partner
    have this setup properly.

 7. Update the <code>README.md</code> in your project directory to contain the 
    following information at the top of the file (updating it with your own 
    information:

    ```markdown
    # Project Submission

    Author: YOUR NAME (LAST 3 DIGITS OF 810 NUMBER HERE)

    [If you did any of the exra credit then please indicate that here.]
    ```
        
## Extra Credit Project Tasks

You may earn up to 5 points extra credit for each of the tasks listed below:

 1. Design and implement your user interface so that the minesweeper game 
    can be used entirely using the keyboard.

 2. Instead of setting text for each button, paint them. This will allow you
    to use cool looking graphics.

 3. Implement a leader board for highschores. You will need to read and write
    to a text file in order to implement this.

## Recursive Minesweeper

This is part is pretty simple, but you are going to have to be very careful so
you don't get a stack overflow exception. When the user clicks on a coordinate,
for each adjacent coordinate, we check the number of adjacent mines. In recursive
minesweeper, if you check an adjacent coordinate and the number of adjacent
mines is zero then you recurse and click on that coordinate as well.

## Design Suggestions

You may design your minesweeper game to look as plain or as cool as you want.

Your user interface should provide the functionality expressed earlier in this
README as well as (at least) the following:

 1. The player should be able to specify the size of the gameboard.
 2. More coming soon!

## Resources

I am pleased to announce that GitHub's Education Liaison, John Britton, has provided 
our class with some private repositories! This gives an excellent opportunity to
practice with version control.

The files for this project are hosted Github using <code>git</code>. They can be
retrieved by cloning the repository found at <code>git@github.com:mepcotterell-cs1302/cs1302-minesweeper.git</code>. 
Since <code>git</code> is a decentralized version control system, you will
have your own local copy of the repository. This means that you can log your 
changes using commits and even revert to a previous revision if necessary. For
this project, using <code>git</code> for version control is part of the project
requirements.

## Directory Structure and Packages

All of the non-test classes for this project should be contained in the <code>src/main/java/cs1302/minesweeper</code>
directory. These classes are in the <code>cs1302.minesweeper</code> package.

The UML designs and GUI mock-ups need to go into a directory called <code>designs</code>. The GUI mockups
should go into the <code>designs/gui</code> directory. The UML class diagrams should go into the
<code>designs/uml</code> directory.

All of the JUnit test classes for this project should be contained in the <code>src/test/java/cs1302/minesweeper</code>
directory. These classes are also contained in the <code>cs1302.minesweeper</code> 
package so that you do not need to do any imports to test your own code.

## Build System

For this project, we will be using the Simple Build System (sbt). If you clone 
the project from the GitHub repository then everything will be setup for you. In 
order to compile your project, you can use the following command:

    $ ./sbt compile

To run your JUnit tests, you may use the following command:

    $ ./sbt test

To run your project, use the following command:

    $ ./sbt run

In order to clean your project (remove compiled code), use the following command:

    $ ./sbt clean

## Submission Instructions

You will still be submitting your project via <code>nike</code>. Make sure your 
work is on <code>nike.cs.uga.edu</code> in a directory called 
<code>LastName1-LastName2-p3</code>, and, from within the parent directory, 
execute the following command:

    $ submit LastName1-LastName2-p3 cs1302a

It is also a good idea to email a copy to yourself. To do this, simply execute 
the following command, replacing the email address with your email address:

    $ tar zcvf LastName1-LastName2-p3.tar.gz LastName-FirstName-p3
    $ mutt -s "[cs1302] p3" -a LastName1-LastName2-p3.tar.gz -- your@email.com < /dev/null

## Questions

If you have any questions, please email them to Michael E. Cotterell at 
<code>mepcotterell+1302@gmail.com</code>

## Frequently Asked Questions

 1. What do I do if the <code>sbt</code> command does not execute?

    You probably need to make the file executable. To do this, simply make sure 
    you are in the same directory as <code>sbt</code> and issue the following
    command:

        $ chmod +x sbt

    This command updates the permissions on the file, making it executable for the
    current user.

 2. When I execute the <code>sbt run</code> command on <code>nike</code>, I get 
    a <code>java.awt.HeadlessException</code> that tells me no X11 DISPLAY 
    variable was set, but this program performed an operation which requires it.
    What is going on and how do I fix it?

    This exception is thrown if you are not running an X server on your computer
    or you are not telling your SSH client how to connect to the X server on
    your computer.

    If you are connecting to <code>nike</code> using a Linux or MacOS X machine
    then you probably already have an X server installed. If that is the case
    then you need to login using the following command:

        $ ssh -X username@nike.cs.uga.edu

    If you are using MacOS X and are unable to resolve your problem simply by
    issuing the above command then follow the directions [here](http://tutorialgenius.blogspot.com/2012/03/how-to-enable-x11-forwarding-with-ssh.html).
    After following the steps on that website, try logging into nike using the 
    SSH command above.

    If you are connecting to <code>nike</code> using PuTTY on Windows then you 
    need to download and install Xming. For information about how to setup Xming
    with Putty, please follow the directions [here](http://blog.nth-design.com/2010/05/19/x11-putty-xming/).
    You may skip some of the steps on that website (e.g., the section on 
    downloading and installing PuTTY), however, please read all of the sections
    related to Xming as wells the sections related to configuring PuTTY.\

