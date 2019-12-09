# Landing
On page load, query the database to see if a session for device is present. If so, return said session and use credentials for operations, resetting the timeout for session. If session is nonexistent, navigate to the home page and prompt user to register or login. Other accessible options may include an ‘about’ page and ‘contact’.

# Register
User is presented with fields for email, first name, last name and password. Form is validated and sent to server. Upon request receival, server will attempt to save the user using ‘passport’. Upon successful creation of user account, the user is presented with notification of success, and prompted to log in.

# Login
User is presented with fields for email and password. Once submitted, server will attempt to authenticate. Upon success, user will be notified of success and navigated to the activity interface. Upon failure, user will be notified and asked to retry. The login option can display a toggle to ask to remain logged in, and the server will store an indefinite session.

# Navigation Bar
Navigation bar present on all screens post login, has links to activity interface, student interface and an option to logout. ‘About’ and ‘contact’ pages can also have links in the navigation bar. If a user is in the middle of performing an action (filling out a form etc), a prompt will be displayed before a link from the navigation bar navigates away from the current page. The logout action will display a confirmation prompt before logging out.

# Student Management
Student interface will house a rather simple set of actions. Students (most likely displayed in a table) are listed, with actions to add, edit or delete. The add and edit actions may be displayed in a modal (bootstrap popup/over) with a simple text field and submit button. The delete action will prompt if a user is sure (also built in a modal, for design coherence). Once the server receives the relevant request, authentication is checked and database is updated, then a relevant response is sent back to the client. Client will then display feedback based on the server response.

# Activity Interface
The more complex of the interactions with the web page, this will house all user interaction with regards to activities. A user will have the option to search for activities based on the values provided in certain filters. This will take all populated parameters and the server will query the database for records matching the criteria. The client will then display these results in a panel.

The add, edit and delete actions will be relatively straightforward. The add action will display a form inside a modal, with all relevant fields exposed for the user to populate. The submit action on this form shall send the information to the server, which will attempt to save the data to the database. The client will display the resulting success or failure feedback from the server. The edit action will show a similar form with certain fields being uneditable, and a similar process will ensue. The delete action will prompt for confirmation before sending the instructions to the server.

# About
The about page may display some information pertaining to the service or company, along with copyright and other information. There should be little to no interactivity with this page.

# Contact
The contact page may display relevant contact information, and may also house a form that can send instructions to the server to send an email along to a server defined email address. This is a preferred option due to the fact that the email address does not have to be publicly exposed, and if needed we can implement a way to prevent spamming through this form.