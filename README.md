PiBBS
=====

About
-----

A web framework, and Forum/BBS web application. It is light-weighted, easy to deploy and extend.

Features include:

 - Provide a web framework for sign up, sign in/out, user profile management.
 - Provide a forum/bbs.
 - Allow fine control of permissions of board and articles.
 - Provide an internal mailbox. 
 - Allow sending external emails and internal emails.
 - Interface works well on desktop, ipad, and mobile devices.
 - Allow creation of new themes, mostly by changing files in /theme and /css.
 - Allow customizable settings, in /conf/conf.php. 
 - Allow English or Chinese version. Easy to extend to other languages.
 
History
-----

Development first initiated in Summer 2013 as a forum for <a href="http://homecox.com">homecox.com</a>. 
It stopped for a while, and was picked up again in Summer 2014.

License
-----
Released under Apache/MIT/BSD/GPLv2 license.

<hr>
<h2>User Documentation</h2>

<h3>U.1 The homepage.</h3>
<p>
The default installation contains five boards: Computer Science, Programming World, 
News, Just for fun, Forum Administration.
</p>

<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/home1_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/home1_en.png" class="screenshot" alt="homepage screenshot"></a>

<h3>U.2 Interface of a board</h3>
<p>
This is the "Forum" view of a board. The "Digests" view shows articles labeled as digests, which
will show in the homepage digest list. The "Marks" view shows articles marked as important.
</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/board1_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/board1_en.png" class="screenshot" alt="board screenshot"></a>

<h3>U.3 Post special tags</h3>
<p>
Post allows only plain text initially. Then special tags are added to make posts more informative. These include:

<ul>
<li>To show a hyperlink:
<br/>@[a href="{your link}"] {text} @[/a]
<li>To show an image:
<br/>@[img src="{image link}"]
<br/>You can also specify the display size:
<br/>@[img src="{image link}" width="400" height="200"]
<li>To show a video (Youtube, Youku etc.):
<br/>E.g., the original link is &lt;iframe width="560" height="315" src=".." .. allowfullscreen&gt;&lt;/iframe&gt;
<br/>Change to: @[iframe width="560" height="315" src=".." .. allowfullscreen]
<li>To show a segment of code:
<br/>@[code] {your code} @[/code]
<li>To show a segment of code is a textarea with adjustable height:
<br/>@[codearea rows=n] {your code} @[/codearea]
<li>To show bold text:
<br/>@[b] {text} @[/b]
<li>To show underlined text:
<br/>@[u] {text} @[/u]
</ul>
</p>


<p>For example, this post contains a video, two images, an underlined line and a line in bold text.
</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/post_tags.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/post_tags.png" class="screenshot"  alt="post tags screenshot"></a>

<p>
Note that these tags used by BBS are also used identically by I-Mail.
</p>


<h3>U.4 Register An Account</h3>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/register_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/register_en.png" class="screenshot"  alt="register screenshot"></a>

<h3>U.5 Sign in</h3>
<p>There are 2 choices: 1) regular sign in, 2) Linkedin sign in.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/login_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/login_en.png" class="screenshot"  alt="login screenshot"></a>

<h3>U.6 User menu and Profile after sign in</h3>
<p>Figure below shows the user menu, and the basic profile page.
Note only those users who are board managers can see the "Manage Boards" entry.
</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/profile_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/profile_en.png" class="screenshot"  alt="profile screenshot"></a>

<h3>U.7 User Avatar</h3>
<p>The user avatar uses universal icon from gravatar.com.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/avatar_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/avatar_en.png" class="screenshot" alt="avatar screenshot"></a>

<h3>U.8 Internal Mail: I-Mail</h3>
<p>There is a internal mailbox (I-Mail) users can use for private communication with other registered users.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/mailbox_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/mailbox_en.png" class="screenshot" alt="I-Mail screenshot"></a>

<h3>U.9 Compose I-Mail</h3>
<p>This shows the interface to compose an internal mail. The user can send group I-Mail to multiple users. 
Attachment is allowed.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/imail_compose_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/imail_compose_en.png" class="screenshot" alt="I-Mail Compose screenshot"></a>

<h3>U.10 User List</h3>
<p>Under the "Forum" menu there is a "User List" submenu. Click on this shows a list of registered users.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/user_list_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/user_list_en.png" class="screenshot" alt="user list screenshot"></a>

<h3>U.11 External Mail: E-Mail</h3>
<p>From the user list one can send an external email to another registered user. The user's registration email is used.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/email_compose_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/email_compose_en.png" class="screenshot" alt="email compose screenshot"></a>


<hr>
<h2>Board Master Documentation</h2>

<p>Some users are appointed as board masters by system administrator. 
A board master manages users and article permissions in a board.</p>

<p>
The possible options on the management of a post are:
<ul>
<li>Top - a top post is shown at the beginning of a board, with an upward arrow.
<li>Readonly - a readonly post cannot be editted or deleted by its author.
<li>Mark - a post labeled as "Mark" when it is of value, and will show in the "Marks" view of the board.
<li>Digest - a post labeled as "Digest" when it is of value to be known by general forum visitors, and 
will show in the "Digests" view of the board.
<li>Hide - a hidden post is not shown on the board view.
<li>Delete - a deleted post is gone.
</ul>
</p>



<h3>B.1 Manage Board Permission</h3>
<p>
Under the user profile menu there is a "Manage Boards" submenu. Click on this shows the page to manage board permissions.
A board can be Private, Hidden, and/or Readonly. </p>

<p>The rules are:
<ul>
<li>Only board members can post in a Private board.
<li>A Hidden board can be seen only by logged in board members.
<li>No one can post in a Readonly board.
</ul>
</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/manage_board_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/manage_board_en.png" class="screenshot" alt="manage board screenshot"></a>

<h3>B.2 Manage Private Board Members</h3>

<p>If a board is private, only approved members can post in this board.
The board master can add or remove a member to/from the board's members.
</p>

<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/manage_board_members_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/manage_board_members_en.png" class="screenshot" alt="manage board members screenshot"></a>


<h3>B.3 Manage Posts</h3>

<p>The board master can manage posts on the board. A board master will see the "Turn On Manage Mode" link below.
</p>

<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_board_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_board_en.png" class="screenshot" alt="boardmaster screenshot"></a>

<p>Turn On Manage Mode, the board master sees the below options:</p>

<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_board_manage_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_board_manage_en.png" class="screenshot" alt="boardmaster manage screenshot"></a>

<p>Click into the post, the board master sees the below options to manage each post individually:</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_post_manage_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/bm_post_manage_en.png" class="screenshot" alt="boardmaster post manage screenshot"></a>


<hr>
<h2>System Administrator Documentation</h2>

<p>
The system administrator manages all the users, boards and posts in the forum.
The system administrator by default has all the permissions of a board master.
</p>


<h3>S.1 System admin interface</h3>
<p>The figure below shows current functions a system administrator has access to.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_en.png" class="screenshot" alt="admin screenshot"></a>


<h3>S.2 Manage users</h3>

<p>
Links involved are:
<ul>
<li>User - manage users, including add/update/delete
<li>UserGroup - manage user group. Two basic groups are: admin, user.
<li>Code register - used only when the registration code feature is used. 
<br/>When the registration code feature is enabled, only invited people with a registration code can register.
<li>User_LinkedIn - manage linkedin binding of users who sign in using their linked in account. 
</ul>
</p>

<h3>S.2 BBS Management</h3>

<p>
Links involved are:
<ul>
<li>Manage BBS Board Tables (add/remove board/forum). This allows to create/edit new board. See S.2.2.
<li>BBS_BoardList (BBS Board List). This lists all the boards.
<li>BBS_BoardGroups (BBS Board Group). This allows to manage board groups. See S.2.1.
<li>BBS_BoardManager (BBS Board Manager). The allows to manage board managers. See S.2.2.
<li>BBS_PrivateMembership. This lists the members in each private board.
</ul>
</p>

<p><b>S.2.1 Manage BBS Board Tables.</b></p>
<p>A board belongs to a group. Use the "BBS BoardGroups (BBS Board Group)" link to manage groups, 
including add/udpate/delete.</p>

<p><b>S.2.2 Manage boards</b></p>
<p>The "Manage BBS Board Tables (add/remove board/forum)" page allows a new board to be created.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_manage_boards_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_manage_boards_en.png" class="screenshot" alt="admin manage board screenshot"></a>

<p>
A new board can be added here. 
</p>

<p>
A board can have 0, 1 or more than 1 managers. Two places are relevant: table BBS_BoardManager and 
table column BBS_BoardList.managers. </p>
<p>
In table 'BBS_BoardList', the 'managers' column format is:
user_id,user_name,role[|user_id,user_name,role]*
</p>


<h3>S.3 IMail Management</h3>

<p>
Links involved are:
<ul>
<li>IMail - mail information (read only).
<li>IMailRecv (Check receive activity) - view receive status (read only).
<li>IMailRecvNotify - view mail notification information (read only).
<li>IMailState - constants for mail state (read only).
<li>IMail email notification - this can send mail notification immediately. 
<br/>This can be set up such that it is done by crontab job automatically periodically.
</ul>
</p>


<h3>S.4 Views</h3>

<p>
Links involved are:
<ul>
<li>View_Log_site (Site Activity Log) - shows site activity log (read only).
</ul>
</p>


<h3>S.5 Management functions</h3>

<p>
Links involved are:
<ul>
<li>Backup Database - see S.5.1.
<li>Generate registration code - used only when the registration code feature is on.
</ul>
</p>

<p><b>S.5.1 Backup Database</b></p>
<p>The allow backup site database from web interface.</p>
<a href="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_backup_db_en.png"><img src="http://cssauh.com/xc/PiBBS/INSTALL/doc/image/admin_backup_db_en.png" class="screenshot" alt="admin backup database screenshot"></a>


<h3>S.6 Reports</h3>

<p>
Links involved are:
<ul>
<li>Registration Code Statistics - used only when the registration code feature is on.
<li>Site Activity - show site activites (read only).
</ul>
</p>


<h3>S.7 configuration file</h3>

<p>
Under the forum directory there is a /conf folder, which contains these configuration files:
<ul>
<li>conf.php
<li>linkedin_conf.php
<li>upload_conf.php
</ul>
</p>

<p><b>S.7.1 conf.php</b></p>

<p>This allows many settings, for example:
<ul>
<li>Site debug mode (if true, show more details in error/warning information)
<li>Database config file location.
<li>Language. Currently support Chinese and English.
<li>Captcha. Use or not. Length of Captch string.
<li>Registration code. Use or not.
<li>User account email activation. Use or not.
<li>Email. Actually send email or not.
<li>Site name, and site master email.
<li>Time zone.
<li>BBS settings. Various.
<li>Gravatar. Use or not.
<li>IMail settings. Various.
</ul>
</p>


<p><b>S.7.2 linkedin_conf.php</b></p>

<p>This file contains linkedin parameters: 
<ul>
<li>API_KEY 
<li>API_SECRET
<li>REDIRECT_URL
<li>SCOPE
</ul>
</p>

<p><b>S.7.3 upload_conf.php</b></p>

<p>
This file contains upload parameters: 
<ul>
<li>Max file size.
<li>Allow file extensions.
<li>Upload file root.
</ul>
</p>


<hr>
<h2>Developer Documentation</h2>

This is a light-weighted, easy to deploy, use and modify website framework.

This section talks about several important aspects if one wants to develop based on this framework.

<h3>D.1 Database development</h3>

<p>To work on the database, one just needs to include either /func/db.php or /func/db_mysqli.php.

<p>These two files implement exactly the same set if API functions.
/func/db.php uses the mysql connection system calls, which is deprecated by MySQL since 2012. 
/func/db_mysqli.php uses the mysqli connection system calls and is preferred.

<p>The API functions:

<ul>
<li>db_open()
<br/>Open a database connection.

<li>db_close()
<br/>Close a database connection.

<li>getScalar($query, $col = '')
<br/>Return a single element in the first row of the returned set.
<br/>If $col is empty, use the first element; otherwise use the named element.

<li>executeScalar($query, $col = '')
<br/>Same as getScalar().

<li>executeNonQuery($query)
<br/>Execute a query that does not return any data.

<li>executeRowCount($query)
<br/>Return number of rows in the returned data set.

<li>executeScalarArray($query, $col)
<br/>Return an array of the given field in the query.

<li>executeDataTable($query)
<br/>Return entire table (requested in query) as a DataTable.
<br/>First row is for column names.
<br/>The rest rows are data.

<li>executeAssociateDataTable($query)
<br/>Return entire table (requested in query) as an associate array.
<br/>Compared to executeDataTable, this shifts the processing to calling function.
<br/>Synopsis: <pre>
   $t = executeAssociateDataTable_2($sql);
   $len = count($t);
   for ($i = 0; $i < $len; ++ $i) {
       $row = $t[$i];
       foreach ($row as $key => $val) {
           print "$key => $val, or value is: $row[$key]";
       }
   }
</pre>

<li>executeAssociateDataTable_2($query)
<br/>Similar to executeAssociateDataTable(), 
but the first row is for header columns, other rows are for data.

<li>executeDataTable_ToHtmlTable($query, $property="", $show_count, $do_htmlencode)
<br/>Given a query, return a html string, showing the return table.
<br/>$query: value is string. the query string.
<br/>$property: value is string. attribute of the table, e.g., class.
<br/>$show_count: value is boolean. whether to show number of row: 1,2, ...
<br/>$do_htmlencode: value is boolean. whether apply db_htmlencode to contents.

</ul>

<p>Other related functions:
<ul>
<li>db_htmlEncode($s)
<br/>To display html/xml open/close tags and other special characters from database in browsers correctly.

<li>db_encode($s)
<br/>To encode a query to database, avoid special characters or sql injection.
</ul>

<h3>D.2 Other library functions</h3>

<p>Other library function files also reside in /func/ directory:

<ul>
<li>ClsPage.php, ClsPage.js
<br/>A class for paging of a long list.

<li>Cls_DBTable.php
<br/>A class for manipulating a database table.
<br/>This class will read from database schema and automatically build the view/edit/verify forms.

<li>Cls_DBTable_Custom.php
<br/>A class for manipulating a database table.
<br/>
<br/>This class will read from database schema and automatically build the view/edit/verify forms.
<br/>Customized from Cls_DBTable with this change:
<br/>1) Instead of providing a list of hidden fields, provide a list of given fields and titles.
<br/>2) Added styles for TB, TR, TD.
<br/>3) Added en/cn languages for buttons.
<br/>
<br/>This is convenient when you want to use custom field titles, and in different languages.

<li>avatar.php
<br/>Use avatar from gravatar.com

<li>captcha.php
<br/>Function to create and use a captcha image made of English letters and digits.

<li>captcha_cn.php
<br/>Function to create and use a captcha image made of Chinese characters.

<li>email.php
<br/>Email functions.

<li>mobile.php
<br/>Decide if the browser client is on mobile device.

<li>util.php
<br/>Various utility functions, such as:
<br/>- Getting GET/POST/REQUEST parameters.
<br/>- String functions: startsWith( $haystack, $needle ), endsWith( $haystack, $needle ), str_truncate($s, $maxlen).
<br/>- Get random string: getRandStr($len, $type=1)
<br/>- Convert array to/from selection list.

<li>util_fs.php
<br/>File system utility functions. Such as:
<br/>- create/delete directory/file
<br/>- decide if a directory is empty
<br/>- return files under a directory

</ul>

<h3>D.3 Authentication</h3>

To use the authentication mechanism of this framework is very easy,
just include certain authentication check files under directory /func.

<ul>
<li>/func/auth.php
<br/>Check if a user has signed in.
<br/>Synopsis: <pre>
&lt;?php
session_start();
require_once("../func/auth.php");
?&gt;
</pre>

<li>/func/auth_board_manager.php
<br/>Check if a signed in user is a board master.
<br/>Synopsis: <pre>
&lt;?php
session_start();
require_once("../func/auth.php");
require_once("../func/auth_board_manager.php");
?&gt;
</pre>

<li>/func/auth_admin.php
<br/>Check if a signed in user is a system administrator.
<br/>Synopsis: <pre>
&lt;?php
session_start();
require_once("../func/auth.php");
require_once("../func/auth_admin.php");
?&gt;
</pre>
</ul>

<h3>D.4 Themes</h3>

<p>
This framework allows a central place to create and use new themes in the /theme and /css directory.
</p>

<p>The /theme folder contains these files:
<ul>
<li>header.php, footer.php
<br/>To be included in any other web interface files, for a consistent look.

<li>themes.php
<br/>This is where a theme is defined and used.
<br/>Based on the theme name, different css files from /css folder is used.
<br/>Here you can define page title, keywords, description, forum's top row banner image and other elements.

<li>share.php
<br/>Include this to display the social media share icons from jiathis.com.
<br/>This file is included in footer.php by default. You can include it in other places too.
</ul>
</p>

<p>The /css folder contains css files for different themes.
<ul>
<li>Right now there are 2 themes: 1) plain and 2) blue. "blue" is the default theme.
</ul>
</p>

<p>To create a new theme, you need to:
<ul>
<li>Change /theme/themes.php, for forum's top row banner image and other elements
<li>In /css, create a new sub-directory, with these css files:
<br/>a) digest.css (for bbs digest), 
<br/>b) menu.css (for menu), bbs.css, 
<br/>c) bbs_mobile.css (for bbs, both desktop and mobile versions), 
<br/>d) site.css, site_mobile.css (for entire site, both desktop and mobile versions).
</ul>
</p>

<h3>D.5 File Upload</h3>

<p>There are currently two places that upload is used: 1) BBS, 2) I-Mail.</p>

<p>
Currently file upload works this way: 
<ul>
<li>A file is first uploaded to a temprary folder,
then copied to final folder when the user submit the BBS post or I-Mail. 
<li>The temp folder is in /upload/[function]/tmp, and final folder is in /upload/[function]/fin.
<li>Under the /tmp or /fin directory, user's username is used as storage folder.
</ul>
</p>

<p>
Security:
<ul>
<li>For security purpose, an uploaded file's url cannot be easily guessed. 
<li>For this, a salt,
which is a random string of length ~10 is generated for each BBS post or email, and used
as the part of the the storage folder name.
<li>This way it's very hard to guess the url of the uploaded file.
</ul>
</p>

<p>To create a new upload function, one needs to:
<ul>
<li>Add corresponding storage folders in /upload
<li>Include files file_upload.php, attachment_func.php as in /bbs and /imail, and make corresponding changes.
<li>BBS and I-Mail's upload functions can be used as examples to understand how to implement a new upload function.
</ul>
</p>


<h3>D.6 Miscellaneous</h3>

<p><b>D.6.1 Google Analytics</b></p>

You can include your analytics code in /js/analytics.php, which is included in theme/footer.php by default.

<p><b>D.6.2 Social media promotion icons</b></p>

The jiathis.com icon panel is used. The code is in /theme/share.php and included in theme/footer.php by default.



<hr>
<h2>To-do List</h2>

<h3>IMail</h3>
<ul>
<li>email notification on imail (done. also set up cron job for this)
<li>admin send mail to all members
<li>draft
<li>upload progress by javascript
<li>cc, bcc
<li>receipt notification to sender
</ul>

<h3>EMail</h3>
<ul>
<li>group mail (done)
<li>attachment
</ul>

<h3>Wiki post</h3>
<ul>
<li>wiki post: everyone can edit.
</ul>

<h3>More of user profile</h3>
<ul>
<li>In addition to current basic profile, provide a page to get more user details.
</ul>


<h3>BBS post tag buttons</h3>
<ul>
<li>So user no need to type tags manually 
<li>email notification of response
<li>email notification of new post
</ul>


<hr>
<h2>Author</h2>

X. Chen <br/>
Copyright &copy; 2013-2014<br/>

Contact: 
<a href="mailto: homecoxoj@gmail.com">Email</a> | 
<a href="https://github.com/chenx/PiBBS">Download</a>
