## This website is the personal project of yours truly.
<br>

I wrote it from scratch, and as such it is very experimental. 

What it runs on:
- Backend
- AWS on the backend, in this order:
- API Gateway 
- a single Lambda function powering the whole site		- content served from an S3 bucket- Frontend	- Aurelia (a little known framework)	- hosted on an S3 bucket  How its designed:- Backend	- the Lambda is organized around a `Blogpost` model (I should add more here)- Frontend	- standard Aurelia project format (I should add more here)Why I did it:- I want to get more experience across both ends of the stack, so this is my attempt at doing so. - I want to get better at designing large software projects, so as this site grows in complexity I want to manage it well.- the old site (link forthcoming) was pretty _greasy_, to say the least.------### Why does the 'Loading' on the home page take so long?Since I'm working with C# Lambdas on the backend, I can only return one kind of object, an instance of a `BlogPost`.I am displaying a list of `BlogPosts` on the home page, however; this means I must make one request per post to populate the entire list.You can open up the Network tab of Devtools to see this in sad action.This is terribly inefficient.What would serve much better is  _another_  Lambda that was responsible for serving content suitable to the home page, namely, a `List<BlogPost>`.I will do this. I don't have time right now, but I will do this.-----Drop me a line, for whatever reason: dsabbaghumd AT gmail DOT com.
