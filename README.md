## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
	
 	```
	1. Protocol - sets http or https
	2. domain - the local host
	3. port 
	4. path - the path within the domain you want
	5. query string
	6. anchor tag - the part on the webpage you would like to access 
	```
	
* Name the pieces of the following urls:
	* `https://www.google.com/`
	
	```
	Protocol://domain
	```
	
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367`
		
	```
	Protocol://domain/path
	```
	
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy`
		
	```
	protocol://domain:port/path?queryString#anchortag
	```
	
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
		
	```
	protocol://domain/path#anchortag
	```	
	
* Can a server use more than 1 prt? 

	```
	Yes.
	```

* Why is https different than http?
	
	```
As compared to http, when using HTTPS, the computers agree on a "code" between them, and then they scramble the messages using that "code" so that no one in between can read them.
	``` 

* How does a server interpret the following url's query paramter.  What data structure does it create on the server?

	```
	http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
	```
		
	```
	It creates an array named puppies with elements of fido, max, and moxie.
	```

__HTTP Request/Response__

* Name at least 4 http verbs

	```	
	Get, post, delete, put, patch
	```

* What is each verb useful for in your own words

	```
	Get - get info from a server
	Post - post/send info to a server
	Delete - delete info from a server
	Patch/Put - change an existing resource on a server. 
	```

* What does idempotent mean?

	```
	that the operation does not change the data.
	```

* Name the 5 http status code ranges.  What are they used for in general?

	```
	100 - Getting there soon
	200 - ok
	300 - redirect
	400 - client side error
	500 - server side error
	```

* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?

	```
	it permanently redirects the request.
	```

* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept 
	
	```
	Request
	```
	
	* Content-type 
	
	```
	Response
	```
	
	* User-agent
	
	```
	Request
	```
	
	* Set-cookies 
	
	```
	Response
	```
	 
	* Cache-control
	
	```
	Both
	```
	
	* Cookie
	
	```
	Request
	```
	
	
* Is the following a http request or response?  How do you know for each?

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: *
Vary: Accept
Content-Type: text/html; charset=utf-8
Content-Length: 722
ETag: W/"2d2-Wu0We9N5g35FXWY+gOATLA"
Date: Tue, 08 Mar 2016 20:37:11 GMT
Connection: keep-alive

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/style.css">
    <title>Student Roster</title>
  </head>
  <body>
    <main>
      <h1>Student Roster</h1>
      
        <section>
          <h3>Daenerys Targaryen</h3>
          <span>Student Id: nys8fbohl</span>
          <h4>Hobby: Motherhood</h4>
          <img src="https://i.imgur.com/KlycRG5.jpg" alt="Daenerys Targaryen" />
        </section>
      
        <section>
          <h3>Tyrion Lannister</h3>
          <span>Student Id: njehukbohe</span>
          <h4>Hobby: Traveling</h4>
          <img src="https://i.imgur.com/fFMusdC.png" alt="Tyrion Lannister" />
        </section>
      
    </main>
  </body>
</html>
```
```
This is a response as there is a content-type header and it's returning the HTML structure of a page.
```


```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```

```
This is a request as DELETE is a request verb
```


__JSON__

* Describe what JSON is.  What is it used for.

```
JSON is JavaScript Object Notation which is a string of data that is used to exchange data on the web.
```

* Convert the following map into a javascript object then console log the age.

```
{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
```

```
var GitHub = JSON.parse('{ "company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}');
console.log(Github.age);
```

* Convert the following to a javascript object.  Console log each company name.

```
{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}
```
* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};
```
```
console.log(JSON.stringify(myObj));
```

__MISC__

* Describe what DNS is.
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).
* What is TCP/IP?  How does it interact with HTTP?
* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
