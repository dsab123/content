### Hi! I’m a software developer living on the east coast. 

### I wrote this website from scratch (i.e. no WordPress, Squarespace — just me and my code), and I write about books and spiritual things.

### If you’ll listen, I want to tell you how I got to the point of releasing this blog into the wild, and why that matters to you, the reader.
<br>

I see my progression to writing this blog in three stages. First, my awakening to **spiritual things**; second, my embrace of **reading**; and third, the publishing of my **writing**.
<br>

### Spiritual Things
I had very unsettled years, spiritually speaking, from about the time I was eighteen until about twenty-one. After a crisis of faith, I came to a settled understanding of the Christian religion. I found a solid church home (Trinity OPC peeps, I love you and miss you all so much) and began to learn spiritual things at a rapid pace.
<br>

### Reading
I soon embraced reading as a spiritual discipline. I picked up Bibles and theology books wherever I could find them (shoutout to Value Village in PG), and began reading voraciously. Popular-level theology books were my mainstay for a while, but soon after I picked up church history surveys. Puritan works soon followed, which showed me <a href="https://danielsabbagh.com/#/blog/15/o-consider-his-loveliness-and-beauty" target="_blank">the loveliness and beauty of Christ</a>. After reading <a href="https://danielsabbagh.com/#/summary/4/lit">a book about reading books</a>, I learned that it was not a spiritually ‘lesser’ practice to read secular books. So I branched back into fiction and some classics, and the occasional bestseller. And when I started seminary, I added graduate-level books to the mix. A pretty wide span, eh?
<br>

### Writing
Not too long after I began reading, I found myself writing. Mostly about those spiritual things, mostly in Evernote, mostly for myself. I wrote prayers, notes from my own studies in the Bible, thoughts on books I was reading, and the like. Writing became an invaluable tool for grappling with what I was consuming, or what I was struggling through. And in turn this grappling caused me to grow in my understanding of the topic at hand.
<br>

## Why Blog?
I've had this blog up in some form or another since 2015, and it’s served me well to that end. On the prior incarnation of this <a href="http://old-danielsabbaghcom-website.s3-website-us-east-1.amazonaws.com/blog/2015/why-blog/" target="_blank">about page</a>, I said that my writing was mainly for me and my career, not for you:
<br>

<img src="bed18732698d622b90b9500ebc9c0fc5.jpg" class="post-image" alt="image of old about page" title="Beware the font whiplash and incoherent short sentences">
<br>

I don’t agree with my younger self anymore. If writing aids my communication, as I say in the second sentence, then my writing by definition is for you. Because writing is a form of communication. 
<br>

So I’ll continue to use danielsabbagh.com to practice my writing, but with an eye toward you, the reader of my content.
<br>

And if my writing is for you, I’ll beg the question by asking: What’s in it for you? Why read this blog? Well, If I’m practicing my (spiritual) writing, then you can use my site to practice your (spiritual) reading!
<br>

Stemming from my personal experience, I have a _deep desire_ to encourage folks to keep up some kind of spiritual reading that involves books. Our reading should include more than just christian blogs and podcasts. There is something about engrossing yourself in a book that at times requires sheer effort to work through; this effort is simply not required in other mediums. Blogs, tweets, facebook posts, podcasts simply do not compare (although podcasts might come the closest). 
<br> 
In the online mediums, the writer is often concerned about page views and the spread of their content, so any phrase or word that won’t tend to that end gets removed. Or, if you disagree you can just close your browser and find another article. But with a book, you’re bound to find something you disagree with, and if you’re diligent you’ll grow in your own perspective as you wrestle with new ideas.
<br>

Plus, you’ve already bought the book at that point, so the author is freed from having to cater to you for money.
<br>

To that end, I plan to blog about spiritual things, and to write book summaries and reviews to encourage you to buy good books. 
<br>

I’ve signed up for Amazon’s affiliate program, which means whenever you buy a book through a link on this site, I get a tiny cut of the profits. The money I’ll be making isn’t a substitute for a real job, but a couple bucks a month would be pretty sweet.
<br>

Please drop me an [email](mailto:dsabbaghumd@gmail.com) letting me know what you think about this endeavor.
<br>

There’s a second reason to the question “Why blog?” The answer is to keep up my software skills, hence this site being written from scratch. If techy things are in your purview, read on. If not, I won’t be offended, ha!
<br>
<br>

## This Site’s Internals
I built this site from scratch! That means I’ve designed everything you’re seeing, from the layout to the loading times to the navigation, and everything in between. This has been a painstaking effort, and has yielded great benefit to my skills. I’m much more of a full-stack developer after working at this site for a few years. I’ve blogged through aspects of the site, but I’m saving most of the technical content I’ve written for another website that I’ll open up later. 
<br>

If you’re of the programming persuasion, here are some cool things about the guts of the site:
<br>

The frontend is 
<br>
  - written in <a href="https://aurelia.io" target="_blank">Aurelia</a>, a snazzy front-end framework
  - bundled with <a href="https://webpack.js.org" target="_blank">Webpack</a>, which I love so much for ease of use; other bundlers are squares
  - deployed to an S3 bucket that sits behind a CloudFront CDN
<br>

The backend is all AWS, which consists of 
<br>
  - an API Gateway that defines resources such as blogpost, booksummary, and the like, with almost all GET requests
  - the API triggers reeeeeeeeaaaalllly simple AWS Lambda functions written in node, which are essentially wrappers around database queries
<br>

The database looks like
<br>
  - a pretty simple RDS Postgres instance that houses metadata like titles, summaries, dates, tags, teaser text, and the like
  - a GitHub repository to store raw article content; AWS is expensive, and GitHub allows 5,000 requests per hour per repo on their free tier 😍
<br>

Though I’m proud of the little infrastructure I’ve built for the site, I don’t think it could handle more than a few hundred users at a time, and not only because I’m on the free tier of everything except RDS. I have plans to robustify the site, which include figuring out
<br>
- how CDNs work with caching images and static assets; I’m getting some cache misses from CloudFront on static assets, which is quite the anomaly
- how to set up some kind of Server-Side Rendering for SEO purposes, which I don’t know how to do right now because I’m running a serverless backend
- looking at Infrastructure-as-Code solutions like Terraform (or Netlify? or Ansible?) to store my AWS infrastructure in source control
- how to use Service Workers to cache blogposts and enable a smoother user experience
<br>

Wow, thanks for reading this far! If the technical aspect interests you I’d love to hear why. <a href="mailto:dsabbaghumd@gmail.com" target="_blank">Email me about it</a>.
<br>

Now, go read my blog and buy some good books.
