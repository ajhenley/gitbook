# Sessions in Servlets and Web Pages

Sessions in Servlets and Web Pages
Session tracking enables you to track a user's progress over multiple servlets or HTML pages, which, by nature, are stateless. A session is defined as a series of related browser requests that come from the same client during a certain time period. Session tracking ties together a series of browser requests—think of these requests as pages—that may have some meaning as a whole, such as a shopping cart application.

HTTP is a "stateless" protocol which means each time a client retrieves a Web page, the client opens a separate connection to the Web server and the server automatically does not keep any record of previous client request.

 Still there are following three ways to maintain session between web client and web server:

 Cookies:

 A webserver can assign a unique session ID as a cookie to each web client and for subsequent requests from the client they can be recognized using the recieved cookie.

 

This may not be an effective way because many time browser does not support a cookie, so I would not recommend to use this procedure to maintain the sessions.

 

Hidden Form Fields:

 

A web server can send a hidden HTML form field along with a unique session ID as follows:

 <input type="hidden" name="sessionid" value="12345">
This entry means that, when the form is submitted, the specified name and value are automatically included in the GET or POST data. Each time when web browser sends request back, then session_id value can be used to keep the track of different web browsers.

 

This could be an effective way of keeping track of the session but clicking on a regular (<A HREF...>) hypertext link does not result in a form submission, so hidden form fields also cannot support general session tracking.

 

URL Rewriting:

 You can append some extra data on the end of each URL that identifies the session, and the server can associate that session identifier with data it has stored about that session.

 For example, with http://tutorialspoint.com/file.htm;sessionid=12345, the session identifier is attached as sessionid=12345 which can be accessed at the web server to identify the client.

 URL rewriting is a better way to maintain sessions and works for the browsers when they don't support cookies but here drawback is that you would have generate every URL dynamically to assign a session ID though page is simple static HTML page.

 The HttpSession Object:

 

Apart from the above mentioned three ways, servlet provides HttpSession Interface which provides a way to identify a user across more than one page request or visit to a Web site and to store information about that user.

 The servlet container uses this interface to create a session between an HTTP client and an HTTP server. The session persists for a specified time period, across more than one connection or page request from the user.

 

 You would get HttpSession object by calling the public method getSession() of HttpServletRequest, as below:

 HttpSession session = request.getSession();
You need to call request.getSession() before you send any document content to the client.