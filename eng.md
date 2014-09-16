There are many great reasons to use Node.js, regardless of experience level.
Take a look into what some of the greatest practical reasons are to use Node and
why you should love it.

I get it. You're not a bandwagon developer. You don't use the cool, trendy
platform just because everyone else is. That's why you haven't looked seriously 
at[Node.js][1] yet. (Or your boss hasn't let you yet.) Well, it's time to look
again. There are many great, practical reasons to use Node. Here are ten of them.

![][2]

### 1. You Already Know JavaScript

Let me guess. You're using a rich client framework ([Angular][3], [Ember][4]
[Backbone][5]) and a REST-ful server-side API that shuttles JSON back and forth
. Even if you're not using one of those frameworks, you've written your own in 
jQuery. So if you're not using Node.js on the server, then you're constantly 
translating. You're translating two things: 1) the logic in your head from 
JavaScript to your server-side framework, and 2) the HTTP data from JSON to your
server-side objects.

By using JavaScript throughout your app, you not only gain mental energy, you
gain practicality as well. By potentially re-using your models, and templates, 
you reduce the size of your application which reduces complexity and chance for 
bugs.

JavaScript as a language is eating the world. It is not going away soon. There
is a JavaScript runtime on every personal computer in the world, and it looks to
stay that way for awhile.

### 2. It's Fast

Node.js is a JavaScript runtime that uses the V8 engine developed by Google for
use in Chrome. V8 compiles and executes JavaScript at lightning speeds mainly 
due to the fact that V8 compiles JavaScript into native machine code.

![][6]

In addition to lightning fast JavaScript execution, the real magic behind Node.
js is the event loop. The event loop is a single thread that performs all I/O 
operations asynchronously. Traditionally, I/O operations either run 
synchronously (blocking) or asynchronously by spawning off parallel threads to 
perform the work. This old approach consumes a lot of memory and is notoriously 
difficult to program. In contrast, when a Node application needs to perform an I
/O operation, it sends an asynchronous task to the event loop, along with a 
callback function, and then continues to execute the rest of its program. When 
the async operation completes, the event loop returns to the task to execute its
callback.

In other words, reading and writing to network connections, reading/writing to
the filesystem, and reading/writing to the database–all very common tasks in web
apps–execute very, very fast in Node. Node allows you to build fast, scalable 
network applications capable of handling a huge number of simultaneous 
connections with high throughput.

### 3. Tooling

![][7]

[npm][8] is the Node.js package manager and it... is... excellent. It does, of
course, resemble package managers from other ecosystems, but npm is fast, robust,
and consistent. It does a great job at specifying and installing project 
dependencies. It keeps packages isolated from other projects, avoiding version 
conflicts. But it also handles global installs of shell commands and platform-
dependent binaries. I can't remember a time with npm where I've had to ask 
myself, "Why are those modules conflicting? Where is that module installed? Why 
is it picking up this version and not that one?
"

[grunt][9] is the venerable task runner, but new kids on the block [gulp][10]
[brunch][11], and [broccoli][12] focus on builds that transform your files, and
take advantage of JavaScript's strong file streams capabilities.

### 4. You Already Know JavaScript, Again

![][13]

So you've decided to use JavaScript on the server, and you're proud of your
decision that avoids all that translating from client data to server data. But 
persisting that data to the database requires even more translations!

There's good news. If you're using an object database like [Mongo][14], then
you can extend JavaScript to the persistence layer as well.

Using Node.js allows you to use the same language on the client, on the server
, and in the database. You can keep your data in its native JSON format from 
browser to disk.

### 5. Real-time Made Easy

If Node.js excels at many concurrent connections, then it makes sense that it
excels at multi-user, real-time web applications like chat and games. Node's 
event loop takes care of the multi-user requirement. The real-time power comes 
thru use of the websocket protocol. Websockets are simply two-way communications
channels between the client and server. So the server can push data to the 
client just as easily as the client can. Websockets run over TCP, avoiding the 
overhead of HTTP.

[Socket.io][15] is one of the most popular websocket libraries in use, and
makes collaborative web applications dead simple. Here's a chat server using 
socket.io:

![][16]

### 6. Streaming data

Traditionally, web frameworks treat HTTP requests and responses as whole data
objects. In fact, they’re actually I/O streams, as you might get if you streamed
a file from the filesystem. Since Node.js is very good at handling I/O, we can 
take advantage and build some cool things. For example, it’s possible to
[transcode audio or video files][17] while they’re uploading, cutting down on
the overall processing time.

Node can read/write streams to websockets just as well as it can read/write
streams to HTTP. For example, we can pipe stdout from a running process on the 
server to a browser over a websocket, and have the webpage display the output in
real-time.

### 7. One Codebase And Your Real-time For Free

If you've made it this far, you may ask yourself, "If Node.js allows me to
write JavaScript on the client and server, and makes it easy to send data 
between the client and server, can I write a web app that runs a single codebase
on both client and server, and automatically synchronizes data between the two?
"

![][18]

The answer to your question would be yes, and the framework for that app would
be[Meteor][19]. Meteor is a next-generation web framework built atop Node. It
runs the same codebase on the both the client and server. This allows you to 
write client code that saves directly to a database. Then, that data is 
automatically persisted to the server. It works the other way too! Any data 
changes on the server are automatically sent to the client. It gets better. Any 
webpage displaying that data reacts automatically and updates itself!

![][20]

### 8. Corporate Caretaker

The inherent risk with any open-source project is abandonment by its volunteer
maintainers. This isn't the case with Node.js. Node is currently sponsored by
[Joyent][21], who has hired a project lead and other core contributors, so
there is a real company backing the future of the project.

### 9. Hosting

![][22]

With rapid adoption, world-class Node.js hosting is also proliferating. In
particular, Platform-as-a-Service (PaaS) providers such as[Modulus][23] and 
[Nodejitsu][24] reduce deployments to a single command. Even the granddaddy of
PaaS, Heroku, now formally supports Node deployments.

### 10. Every Developer Knows (A Little) JavaScript

This one's for your boss.

Since the dawn of the web, there have been JavaScript onclick's and onmouseover
's. Every web developer has coded a little JavaScript, even if that JavaScript 
was hacking a jQuery plugin. Finding web development talent is terribly 
difficult these days. So when choosing a web platform, why not choose the 
platform whose language is known by every web developer in the world?

### In Conclusion, A Bonus!

But wait, there's more! As with any platform or product, open-source or
otherwise, its community is a huge influencing factor. And Node's is second to 
none. From meetups to conferences, there are really smart people working on the 
ecosystem every day. At the same time, the community is welcoming. These same 
smart people are always willing to offer help to folks new to Node, or even 
programming in general. You won't feel bad for asking a question on IRC or 
opening an issue. This community is also very active, with over 91,000 modules 
on npm. And this community is generous. In 2013, individuals
[donated over $70,000][25] to help run the public npm servers.

Yes, Node is trendy at the moment. This is web development, so next week Node
may be dead, and the next hot thing will have arrived (will it be Go or Elixir?
). But give it a try.

=======

This post from Gerard Sychay, a developer over at [Differential][26].
Differential is a great partner of ours and helps companies build and manage 
Meteor applications.

 [1]: http://nodejs.org/
 [2]: img/4c37849586d153a3f3144d94f6243fcb79d77285.png
 [3]: https://angularjs.org/
 [4]: http://emberjs.com/
 [5]: http://backbonejs.org/
 [6]: img/4a020e2b06ef86c0953da6d0092fcd61d5323236.jpg
 [7]: img/56818ee2932a325ff4750d91dbe9f08e95f42876.png
 [8]: https://www.npmjs.org/
 [9]: http://gruntjs.com/
 [10]: http://gulpjs.com/
 [11]: http://brunch.io/
 [12]: https://github.com/broccolijs/broccoli
 [13]: img/02bd613f68f2621611bf8159226cff35b171e066.jpeg
 [14]: http://www.mongodb.org/
 [15]: http://socket.io/
 [16]: img/a815ba9b674ef1131be85ab592c625486deb62cf.png
 [17]: http://transloadit.com/blog/2010/12/realtime-encoding-over-150x-faster/
 [18]: img/9d454db0300752bc526459393453546ec23124f8.png
 [19]: https://www.meteor.com/
 [20]: img/5a2575875b6b23724c0e8f1254b6d27e915275b2.png
 [21]: https://www.joyent.com/
 [22]: img/dc191a6df13cfd174e9cf5da3e6c6877f71bd12b.png
 [23]: https://modulus.io/
 [24]: https://www.nodejitsu.com/
 [25]: https://scalenpm.nodejitsu.com/
 [26]: http://differential.io/