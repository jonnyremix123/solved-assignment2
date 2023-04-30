Download Link: https://assignmentchef.com/product/solved-assignment2
<br>
The LinkedIn Command Line Interface Class

Package: edu.sinclair

LinkedInUser

1) Add two additional private member variables to the LinkedlnUser class:

// holds the last date/time that this user in

java. util. Date lastLogLnDate;

// holds the number of times this user has Logged in

int LoginCounter;

2) Add and implement the following public methods to the LinkedlnUser class:

/**

*Increments the number of times this user has lagged in and assigns today’s

*date to the last Login date.

**/

public void incrementLoginCounter ( ) {

}

// hint: to assign today’s date to a Date type variable, simply create a new

// instance of Date today = new Date ( ) ;

/**

*Returns the number of times this user has Logged in

*@return the login counter.




Public int getLoginCounter ( ) {

}

/**

*Returns the Date that this used last logged in.

*@return the Date.

public Date getLastLoginDate ( ) {

}

LinkedlnCLl

Create a class called, LinkedlnCLl which will serve as the command line interface between the

user and your software. Define the following properties.

/**

*Holds the list of users in the system.

Private List users ;

/**

*Holds the logged in user.

Private LinkedInUser loggedInUser;

Public   LinkedInCLI() {

Users – new ArrayList &lt;&gt; ();

}

The LinkedlnCLl class should have methods to list all the users (i.e. print out their usernames), sign up a new user, delete a user, print who the logged in user is, sign off, and quit.

Create a public static void main method which prints the following menu to the console and awaits user input. Upon entry the application should do the following:

a) Load any previously saved data. See the Serializing and Deserializing section below for the details

b) If there are no users in the system, do the following

<ol>

 <li>Prompt the user to establish the root user and password.</li>

 <li>Default the Linkedlnuser type to “P” for premier and call the newly added incrementLoginCounter () method to establish that this user has logged in once.</li>

 <li>Add the newly created user to the list of users defined within the constructor.</li>

 <li>Assign the newly created user to loggedlnUser property on the class to indicate that this new user is the logged in user.</li>

 <li>Display the Welcome menu (step 2 below).</li>

</ol>

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2019/02/633.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2019/02/633.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>c) If there is at least one user in the system, do the following

<ol>

 <li>Prompt the user to login by supplying a user name and password.If the user name doesn’t exist, display the message, “There is no user with that user name” and re-display the login prompt.</li>

 <li>If the user does exist and the password is incorrect, display the message, “Password mismatch” and re-display the login prompt.</li>

 <li>If both username and password are valid</li>

 <li>Call the newly added incrementLoginC0unter() to increment the number of times this user has logged in</li>

 <li>Assign the user to loggedlnUser property on the class to indicate that this is the logged in user. display the Welcome menu (step 2 below).</li>

 <li>Please login to continue.User namedougPlease supply the users’ passworddoug

  <ol start="2">

   <li>Display the Welcome menu.</li>

  </ol>Welcome logged in user nameList all Users,Sign up a New User,Delete a User,Who am ISign OffQuit(substitute the actual logged in user name for the logged in user name text). </li>

</ol>

Menu Options

List all Users

Loop through all the Linkedln users and print their user name to the console.




Sign up a New user

<ul>

 <li>Prompt the user for the user name to add. Check if the supplied user name already exists in the users list. If it does, display an error message to the console and re-display the menu.</li>

 <li>If the supplied user name is unique, do the following</li>

 <li>prompt the user to enter a password and what type of user he/she is</li>

 <li>Valid types are “S” for Standard and “P” for Premier. If the user enters any other value, display the message, “Invalid Valid types are p or S” and redis I the menu.</li>

</ul>

Enter a username

Enter a password

Enter the type Of user (P or S)

Invalid user type. Valid types are P or S

<ul>

 <li>Construct a LinkedInUser instance and add the instance to the users list on the LinkedInCLI class.</li>

 <li>Serialize your list Of LinkedInlJser Objects to save the newly added user.</li>

 <li>Afterwards, re-display the menu.</li>

</ul>

Delete a User

<ul>

 <li>Prompt for the user name to delete. Check if the supplied user name exists in the user</li>

 <li>If the user does NOT exist, display an error message to the console and re-display the menu.</li>

 <li>If the user does exist, prompt for the password of the user being deleted.</li>

 <li>If the password is not correct, display an error message to the console and re-display the menu.</li>

 <li>If the password is correct, remove the user from the users list. Serialize your list of Linkedlnuser Objects to save the new list, and re-display the menu.</li>

 <li>If the deleted user was the logged in user, null out the loggedInUser on the LinkedInCLI class and represent the user interface.</li>

 <li>Since the logged in user is now null. the application should act the same as the application did upon Start up (either making the user establish a root user or login with an existing user). See step I b.</li>

 <li>Who am IDisplay the following logged in user informationo The usernameo The usero The last logged in date/time. Use the java. text.SimpIeDateFormat class to format the date/time to be printable.o The login countlast:nggedInDateLogged In:Sign a userSign OFFLast In: zmg-øl-zzSign off

  <ul>

   <li>Null out the loggedlnUser property and re-present the user interface.</li>

  </ul>Since the logged in user is now null, the application should act the same as the  application does upon Start up (either making the user establish a root user or login With an existing user). See step I b.</li>

</ul>