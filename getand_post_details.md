<!--
todo: find get/post example app
-->
###What happens when you submit a form?

The example application below will show you the results of submitting a form via Get and via Post. The index page contains two forms. The only difference between the two forms is one sends its data via get and the other via post. Create this project in Eclipse. Once you run it you will get a better understanding of get and post and the Request object which comes from the browser. 

The GET method sends form information via the URL. When using the GET method the 3rd section of the request packet, the request body, remains empty.

The POST method is used when you create an HTML form, and request method=POST as part of the tag. The POST method allows the client to send form data to the server in the request body section of the request. The data is encoded and is formatted similar to the GET method. The data is sent to the server via standard input.

Let's see this actually work. Create the following form in a page called index.html.
{%ace edit=true, lang='html'%}
<form action="ShowRequestHeaders" method="post">
        <!-- hidden input to let servlet know which form was used -->
        <input type="hidden" name="hiddenAction" value="postFormSubmission">

        <label>Email:</label>
        <input type="email" name="email" required value=""><br>

        <label>First Name:</label>
        <input type="text" name="firstName" required value=""><br>

        <label>Last Name:</label>
        <input type="text" name="lastName" required value=""><br>

        <label>&nbsp;</label>
        <input type="submit" value="Join Now" id="submit">
    </form>
    <p/>
    <form action="ShowRequestHeaders" method="get">
        <!-- hidden input to let servlet know which form was used -->
        <input type="hidden" name="hiddenAction" value="getFormSubmission">

        <label>Email:</label>
        <input type="email" name="email" required value=""><br>

        <label>First Name:</label>
        <input type="text" name="firstName" required value=""><br>

        <label>Last Name:</label>
        <input type="text" name="lastName" required value=""><br>

        <label>&nbsp;</label>
        <input type="submit" value="Join Now" id="submit">
    </form>
{%endace%}

<div style="page-break-after: always;"></div>
Next, Create a servlet and replace both doGet and doPost with the following code
{%ace edit=true, lang='html'%}
protected void doGet(HttpServletRequest request, 
			HttpServletResponse response) 
					throws ServletException, IOException {
		printOutput(request,response);
	}

	protected void doPost(HttpServletRequest request, 
			HttpServletResponse response) 
					throws ServletException, IOException {
		printOutput(request,response);
	}
	
	private void printOutput(HttpServletRequest request, 
			HttpServletResponse response) throws ServletException, IOException{
		
		response.setContentType("text/html");
		PrintWriter out = response.getWriter();
		
		String title = "Showing Request Headers";
		out.println("<html><head><title>" + title + "</title></head>"
				+ "<body bgcolor=\"#aed6f1\">\n" + "<h1 align=\"center\">" + title
				+ "</h1>\n" + "<b>Request method: </b>" + request.getMethod()
				+ "<br>\n" + "<b>Request URI: </b>" + request.getRequestURI()
				+ "<br>\n" + "<b>Request Protocol: </b>"
				+ request.getProtocol() + "<br><br>\n"
				+ "<table border=\"1\" align=\"center\">\n"
				+ "<tr bgcolor=\"#ffad00\">\n"
				+ "<th>Header Name<th>Header Value");
		Enumeration<String> headerNames = request.getHeaderNames();
		while (headerNames.hasMoreElements()) {
			String headerName = (String) headerNames.nextElement();
			out.println("<tr><td>" + headerName);
			out.println("    <td>" + request.getHeader(headerName));
		}
		// Read from request
	    StringBuilder buffer = new StringBuilder();
	    BufferedReader reader;

		reader = request.getReader();
	    String line;
	    while ((line = reader.readLine()) != null) {
	        buffer.append(line);
	    }

	    String data = buffer.toString();
		
		out.println("<tr><td>request variables:</td><td>" + data + "</td></tr>");
		out.println("</table>\n");
		out.println("</body></html>");
	}

{%endace%}
 

