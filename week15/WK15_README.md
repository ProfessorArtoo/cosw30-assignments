<p style="color: crimson; font-style: italic;">This assignment will count as both lab and homework for this week.</p>
<hr />
<h2 style="font-size: 24px;">Start Here</h2>
<p><strong>https://github.com/ProfessorArtoo/cosw30-assignments/tree/main/week15</strong><br />You can use the code found in this repo to create the login system for your site. Keep in mind that you may need to alter some of the information to work with your setup.</p>
<p>&nbsp;</p>
<h3 style="font-size: 18px;">A New Connection File</h3>
<p>Notice that we are using a different file for our database connection, 'mysqli_connect.php'. Also, notice the location of the 'mysqli_connect.php' file. It is located outside of the main folder of this site. We could have modified this assignment to use our trusty friend 'dbconnection.php', but it seemed quicker just to use the file provider by the author.</p>
<pre>  &lt;?php # Script 9.2 - mysqli_connect.php

// This file contains the database access information.
// This file also establishes a connection to MySQL,
// selects the database, and sets the encoding.

// Set the database access information as constants:
define('DB_USER', 'u5cvzomu5pwpb');
define('DB_PASSWORD', 'cosw30!2025');
define('DB_HOST', '127.0.0.0');
define('DB_NAME', 'dbu8zpdkawjv9e');

// Make the connection:
$dbc = @mysqli_connect(DB_HOST, DB_USER, DB_PASSWORD, DB_NAME) OR die('Could not connect to MySQL: ' . mysqli_connect_error() );

// Set the encoding...
mysqli_set_charset($dbc, 'utf8');
</pre>
<p>&nbsp;</p>
<h3 style="font-size: 18px;">Check These Items</h3>
<p>You may also need to check the 'SELECT' statement in the 'login_functions.inc.php' include file. Make sure the 'SELECT' statement reflects the specifics of your database and that you have removed the SHA function for the password.</p>
<pre>  &lt;?php # Script 12.2 - login_functions.inc.php
// This page defines two functions used by the login/logout process.

/* This function determines an absolute URL and redirects the user there.
 * The function takes one argument: the page to be redirected to.
 * The argument defaults to index.php.
 */
function redirect_user($page = 'index.php') {

	// Start defining the URL...
	// URL is http:// plus the host name plus the current directory:
	$url = 'http://' . $_SERVER['HTTP_HOST'] . dirname($_SERVER['PHP_SELF']);

	// Remove any trailing slashes:
	$url = rtrim($url, '/\\');

	// Add the page:
	$url .= '/' . $page;

	// Redirect the user:
	header("Location: $url");
	exit(); // Quit the script.

} // End of redirect_user() function.


/* This function validates the form data (the email address and password).
 * If both are present, the database is queried.
 * The function requires a database connection.
 * The function returns an array of information, including:
 * - a TRUE/FALSE variable indicating success
 * - an array of either errors or the database result
 */
function check_login($dbc, $email = '', $pass = '') {

	$errors = []; // Initialize error array.

	// Validate the email address:
	if (empty($email)) {
		$errors[] = 'You forgot to enter your email address.';
	} else {
		$e = mysqli_real_escape_string($dbc, trim($email));
	}

	// Validate the password:
	if (empty($pass)) {
		$errors[] = 'You forgot to enter your password.';
	} else {
		$p = mysqli_real_escape_string($dbc, trim($pass));
	}

	if (empty($errors)) { // If everything's OK.

		// Retrieve the user_id and first_name for that email/password combination:
		//$q = "SELECT user_id, first_name FROM users WHERE email='$e' AND pass=SHA2('$p', 512)";
        $q = "SELECT user_id, first_name, role FROM users_tbl WHERE email='$e' AND password='$p'";
		$r = @mysqli_query($dbc, $q); // Run the query.

		// Check the result:
		if (mysqli_num_rows($r) == 1) {

			// Fetch the record:
			$row = mysqli_fetch_array($r, MYSQLI_ASSOC);

			// Return true and the record:
			return [true, $row];

		} else { // Not a match!
			$errors[] = 'The email address and password entered do not match those on file.';
		}

	} // End of empty($errors) IF.

	// Return false and the errors:
	return [false, $errors];

} // End of check_login() function.
</pre>
<p>&nbsp;</p>
<h3 style="font-size: 18px;">Requirements</h3>
<ul>
    <li>Take the code provided in the repo to create a login system on your site.</li>
    <li>Be sure to create this project in a 'week15' folder.&nbsp;</li>
    <li>Note and replicate folder/file structure demonstrated in the repo.</li>
    <li>Create a functioning login system.&nbsp;</li>
</ul>
<h3 style="font-size: 18px;">How to Submit</h3>
<ul>
    <li>Send the URL to your 'index.php' for your login system.</li>
    <li>Provide credentials to login to your system for testing.</li>
</ul>

<p>This is a change</p>