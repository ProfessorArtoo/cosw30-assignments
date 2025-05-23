<p>&nbsp;</p>
<h3><strong>Site Objectives</strong></h3>
<p>Create a website that sells a product and includes the ability to track products and orders. The site must support login functionality for users with the roles of <strong>customer</strong>, <strong>employee</strong>, or <strong>admin</strong>.</p>
<ul>
    <li>
        <p><strong>Admins</strong> must be able to view, add, and edit users and products, as well as view all orders.</p>
    </li>
    <li>
        <p><strong>Employees</strong> must be able to view all users, products, and orders, and be able to add and edit products.</p>
    </li>
    <li>
        <p><strong>Customers</strong> (the default role) can view only their own information and orders, as well as all available products.</p>
    </li>
    <li>
        <p><strong>Anyone</strong> (even without logging in) should be able to view the list of products.</p>
    </li>
</ul>
<h4><strong>Roles Required</strong>: <code>customer</code>, <code>employee</code>, <code>admin</code></h4>
<ul>
    <li>
        <p>Allow image uploads for either products and users.</p>
    </li>
    <li>
        <p>Display uploaded images in the list view for each corresponding item.</p>
    </li>
</ul>
<blockquote>
    <p>Please send credentials for a <strong>customer</strong>, <strong>employee</strong>, and <strong>admin</strong> account.</p>
</blockquote>
<hr />
<h3><strong>The Breakdown &ndash; This Site Will Contain&hellip;</strong></h3>
<ul>
    <li>
        <p>A login system to access the site.</p>
    </li>
    <li>
        <p>Functionality to view, add, and edit users and products.</p>
    </li>
</ul>
<hr />
<h3><strong>The Database</strong></h3>
<p>Database tables must include the following minimum columns:</p>
<p><strong>Users Table</strong></p>
<ul>
    <li>
        <p><code>user_id</code> (primary key)</p>
    </li>
    <li>
        <p><code>first_name</code></p>
    </li>
    <li>
        <p><code>last_name</code></p>
    </li>
    <li>
        <p><code>email</code></p>
    </li>
    <li>
        <p><code>password</code></p>
    </li>
    <li>
        <p><code>role</code></p>
    </li>
    <li>
        <p><code>status</code></p>
    </li>
    <li>
        <p><code>date_created</code></p>
    </li>
    <li>
        <p><code>last_login</code></p>
    </li>
    <li>
        <p><code>image</code> (optional)</p>
    </li>
</ul>
<p><strong>Products Table</strong></p>
<ul>
    <li>
        <p><code>product_id</code> (primary key)</p>
    </li>
    <li>
        <p><code>product_name</code></p>
    </li>
    <li>
        <p><code>cost</code></p>
    </li>
    <li>
        <p><code>description</code></p>
    </li>
    <li>
        <p><code>date_created</code></p>
    </li>
    <li>
        <p><code>last_login</code></p>
    </li>
    <li>
        <p><code>image</code> (optional)</p>
    </li>
</ul>
<p><strong>Orders Table</strong></p>
<ul>
    <li>
        <p><code>order_id</code> (primary key)</p>
    </li>
    <li>
        <p><code>product_id</code> (foreign key)</p>
    </li>
    <li>
        <p><code>user_id</code> (foreign key)</p>
    </li>
    <li>
        <p><code>date_created</code></p>
    </li>
    <li>
        <p><code>last_login</code></p>
    </li>
</ul>
<hr />
<h3><strong>The Site</strong></h3>
<ul>
    <li>
        <p><span style="font-weight: 400;">Need to have a login, login confirmation and logout pages.&nbsp;</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">Once logged in, sessions control what items are visible based on the users role.</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">There needs to be a place to view all the user, products, and orders as needed.</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">The user list should show ID, Name, Email, Status, Role and image if applicable.</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">The products list should show ID, Name, Cost and image if applicable.</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">The orders list should show the ID, Persons Name and Email, Products Name and cost.</span></p>
    </li>
    <li>
        <p><span style="font-weight: 400;">There should be a page to add and edit users and products. </span></p>
    </li>
</ul>
<hr />
<h3><strong>What to Submit</strong></h3>
<ul>
    <li>Screenshots of your database tables. I need to see all columns, not necessarily all rows.</li>
    <li>
        <p>A ZIP file containing your entire site, including screenshots or database tables. Submit via the file upload in Canvas.</p>
    </li>
    <li>
        <p>A URL to your deployed site.</p>
    </li>
    <li>
        <p>Login credentials for one user in each role (customer, employee, admin).</p>
    </li>
</ul>
<hr />
<h3><strong>Point Breakdown</strong></h3>
<table style="border-collapse: collapse; width: 900px;" cellpadding="6px">
    <thead>
        <tr>
            <th style="width: 94.2687%;"><strong>Criteria</strong></th>
            <th style="width: 5.72048%;"><strong>Points</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="width: 94.2687%;">Well-designed layout (color scheme, custom fonts, clean design)</td>
            <td style="width: 5.72048%;">30</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Tables built correctly</td>
            <td style="width: 5.72048%;">50</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Add user</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Add product</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Add order</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">View user</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">View product</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">View order (must show product details and customer name/email using a JOIN between user and product tables)</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Edit user</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Edit product</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Navigation works across all pages</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Upload image</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">View image in list</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Create login/logout system using sessions (not cookies)</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
        <tr>
            <td style="width: 94.2687%;">Restrict page access using sessions</td>
            <td style="width: 5.72048%;">10</td>
        </tr>
    </tbody>
</table>
<hr />
<h3><strong>Extra Credit</strong></h3>
<table style="border-collapse: collapse; width: 900px;" cellpadding="10px">
    <thead>
        <tr style="height: 26.8892px;">
            <th style="width: 750.67px; height: 26.8892px;"><strong>Criteria</strong></th>
            <th style="width: 148.42px; height: 26.8892px;"><strong>Points</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr style="height: 28.8778px;">
            <td style="width: 750.67px; height: 28.8778px;">Edit order functionality</td>
            <td style="width: 148.42px; height: 28.8778px;">10</td>
        </tr>
        <tr style="height: 28.8778px;">
            <td style="width: 750.67px; height: 28.8778px;">Password hashing</td>
            <td style="width: 148.42px; height: 28.8778px;">10</td>
        </tr>
    </tbody>
</table>
<p>&nbsp;</p>