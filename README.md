# Server-Side Development with Node.js
Well, well... You've taken your first step into a much larger world! Now we find ourselves on the "server side", that ominous term you have perhaps imagined as some amorphous blob of a thing with no definition, no tangibility. Now we can start to change those perceptions. The differences between the client side and the server side may seem confusing, but once we have some terminology out of the way, it gets easier.

## What's server-side development?
Most of the code you've written up until now has run in the browser. When you launch your React apps and type `localhost:3000` in a browser's URL bar, your browser requests and receives a bundle of JavaScript, which it then runs using the browser's JavaScript runtime. But now, as we journey into this new realm, imagine stepping through the wardrobe into Narnia or passing through the Stargate. In the next few months, the code you'll be crafting won't run in the browser anymore. Instead, it will operate in the Node.js runtime on a server. So, what's server-side development? It's simply writing code that runs outside of the browser, on a server somewhere. "To infinity and beyond!" as Buzz Lightyear would say, it's time to expand your coding universe.

## What's a server?
Fair question. For web development, "server" has two meanings which are relevant to you.

1. The hardware on which a server-side application runs. This could be a physical server in a data center, a virtual machine (that is also running on a physical server somewhere), or for most developers when they are building and testing their applications locally, the developer's own computer. (Hey, this means you too! You're a software developer!) So as far as this definition goes for you, your computer is the physical server.
2. *Server* can also mean a piece of software that runs on a physical server, listens for network requests, and then decides what to do with the request. If everything goes well, this usually means providing some kind of response.

Think of it like the Millennium Falcon: sometimes it's the ship (hardware), and sometimes it's Han Solo and Chewbacca running the show (software). Either way, they're ready to respond to whatever the galaxy throws at them.

You have already been using and interacting with a number of web servers in the client-side part of the course:

1. You might not be surprised to find out that `serve` is an application that runs a web server. When it starts, it will look for content in whatever directory you supplied when you start the application.
2. When you run `npm run dev`, the Vite development server listens for requests to `localhost:5173` and returns all of the JavaScript needed to run your React app in the browser.
3. `json-server` is a program that listens for network requests and tries to map the URL of the network request to data in a provided JSON file. We are going to talk a lot more about this idea of mapping routes (URLs) to data resources later in the course.

Think of these tools like the tools Frodo used on his journey—each serving a specific purpose to help you on your quest. Just as the One Ring needed different allies and strategies to reach Mount Doom, your applications need different servers to deliver their magic to users.

### The Request/Response Cycle
What do all of these servers have in common? They all:

1. Listen for network requests (mostly HTTP requests for our purposes).
2. Decide what to do with the request based on their own code and the data provided in the request.
3. Return some kind of response.

What kind of responses? I'm so glad you asked. All kinds! JavaScript code, JSON, HTML code, PDFs of phone bills, pictures of cats—whatever you want. They can also respond with error messages, or ruder responses like "Unauthorized," "Forbidden," or the dreaded `500: Internal Server Error` (this usually means we messed up our code somehow).

![HTTP Request/Response Cycle](./assets/request-response-cycle.png)

Think of these responses as the various spells a wizard can cast, from summoning a light to illuminating dark paths to conjuring a fireball for defense. Each server, like a wizard, has its own repertoire of responses to meet the needs of its users.

## Web Apps with Node.js/Express/Sequelize
Wait a minute, if `json-server` worked on the front end, can't we just use that forever? Sigh. I wish we could. But no, even its documentation says that it is only for mocking server-side apps. Once our applications are deployed and have a lot of data, or a lot of users, we will need more robust applications for our APIs.

### Node.js
Node.js (along with a SQL database) is a very popular platform with a rich toolchain and development environment for building robust web applications. Building our own APIs (instead of using `json-server`'s automatically generated one) also lets us create custom resources tailor-made for our application's needs. There are a number of things about Node.js that are very different from client-side JavaScript, including:

1. A strong type system with the help of TypeScript (optional but highly recommended). Variables are declared with specific types (like strings or integers), and their type stays the same for their lifetime, among other benefits.
2. The code often involves asynchronous operations and promises, a concept that's vital to managing server-side operations efficiently.

>You will find that despite the many differences, much of the syntax and principles you learned for JavaScript will transfer directly to Node.js.

Think of Node.js as stepping into a new realm, where you wield a more powerful version of the JavaScript you already know. It's like upgrading from a novice wizard to a master sorcerer, ready to craft complex spells (APIs) that are custom-made for your application's unique needs.

![Web API with React Client](./assets/web-api-with-react.png)

### Node.js Runtime
The Node.js runtime will actually run our JavaScript code. A runtime is simply another program that takes our code as input and translates it into instructions that our computers' processors can understand. Just like with servers, you've already been interacting with another runtime: the JavaScript runtime! When we say that our React apps run "in the browser," we really mean the JavaScript engine that comes with the browser. Instead of running in a browser, the Node.js runtime will execute your JavaScript code in a separate process on your computer (or somewhere else if your app is deployed!). The term "Node.js" encompasses more than just the runtime—it includes a wide array of tools and libraries that empower developers to build powerful applications.

>It's crucial to search for documentation or tutorials specifically tailored for Node.js and modern JavaScript practices. Looking for resources labeled for Node.js or ES6 and above ensures you're accessing the most relevant and up-to-date information. This distinction helps filter out outdated practices or code examples that may no longer be applicable to modern Node.js development. Happy coding!

## What this course is not
It is important to point out that despite the name, this course is _not_ exclusively about Node.js. Yes, we will delve into Node.js and utilize Express and Sequelize to construct our applications, but that is not the sole focus of our journey. This course primarily serves as a _web development_ expedition with Node.js as our trusty backend companion. Node.js/Express/Sequelize is a vast and multifaceted realm, far beyond the scope of what we can cover comprehensively in this course. For those seeking deeper understanding, consider exploring the links provided below.

Alright, ready to embark on this adventure? If you're nodding in agreement, let's dive right in. Take some time to ponder the reflections below, and then onward to the [Table of Contents](./TABLE_OF_CONTENTS.md).
___

## ✍️ Reflections
1. Take a moment to examine some of the architecture diagrams presented in this chapter, and challenge yourself to sketch one for your own front-end capstone project. As you progress in your career as a developer, you'll likely encounter numerous opportunities to create architecture diagrams. Identify the different components of your application and visualize how they interconnect.

2. Share your diagram with a colleague and engage in a discussion about the similarities and differences between your architectures. Use this opportunity to reflect on any areas of your app's architecture that remain unclear or mysterious.

3. Make note of any unresolved questions or uncertainties regarding your application's architecture. These can serve as valuable discussion points to revisit with your group and instructor later on.

> Whenever you encounter "Additional Material" or "Additional Material and Exercises" at the end of a chapter, it's not mandatory to work on it immediately before moving on. However, consider exploring these resources during lab days or after class within the same week, as they offer valuable insights beyond the main content of the chapters. Remember, revisiting these materials later in the course becomes less likely the further you progress.


## 🔍 Additional Material
1. [Node.js Official Documentation](https://nodejs.org/en/docs/)
2. [Express.js Official Documentation](https://expressjs.com/)
3. [Sequelize Documentation](https://sequelize.org/master/)
