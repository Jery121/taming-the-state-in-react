# Redux

Redux is one of the libraries that helps you implement sophisticated state management in your applications. It goes beyond the local state (e.g. React's local state). It is one of the solutions you would take in a scaling application in order to tame the state. A React application is a perfect fit for Redux, yet other libraries and frameworks highly adopted its concepts as well.

**Why is Redux that popular in the JavaScript community?** In order to answer that question, I have to go a bit into the past of JavaScript applications. In the beginning, there was one library to rule them all: jQuery. It was mainly used to manipulate the DOM, to amaze with animations and to implement reusable widgets. It was the number one library in JavaScript. There was no way around it. However, the usage of jQuery skyrocketed and applications grew in size. But not in size of HTML and CSS, it was rather the size of code in JavaScript. Eventually, the code in those applications became a mess, because there was no proper architecture or frame around it. The infamous spaghetti code became a problem in JavaScript applications.

It was about time for nouveau solutions to emerge which would go beyond jQuery. These libraries, most of them frameworks, would bring the tools for proper architectures in frontend applications. In addition, they would bring opinionated approaches to solve problems. These solutions enabled developers to implement single page applications (SPAs).

Single page applications became popular when the first generation of frameworks and libraries, among them Angular 1, Ember and Backbone, were released. Suddenly, developers had frameworks to build scaling frontend applications. However, as history repeats itself, with every new technology there will be new problems. In SPAs every solution had a different approach for state management. For instance, Angular 1 used the infamous two-way data binding. It embraced a bidirectional data flow. Only after applications grew in size, the problem of state management became widely known.

During that time React was released by Facebook. It was among the second generation of SPA solutions. Compared to the first generation, it was a library that only leveraged the view layer. It came with an own state management solution though: React's local state management.

In React, the principle of the unidirectional data flow became popular. State management should be more predictable in order to reason about it. Yet, the local state management wasn't sufficient at some point. React applications scaled very well, but ran into the same problems of predictable and maintainable state management when building larger applications. Even though the problems weren't as destructive as in bidirectional data flow applications, there was still a problem once the application got larger. That was the time when Facebook introduced the Flux architecture.

The Flux architecture is a pattern to deal with state management in scaling applications. The official website says that *"[a] unidirectional data flow is central to the Flux pattern [...]"*. The data flows only in one direction. Apart from the unidirectional data flow, the Flux architecture came with four essential components: Action, Dispatcher, Store and View. The View is basically the component tree in a modern application. For instance, React is such a View. A user can interact with the View in order to trigger an Action. An Action would encapsulate all the necessary information to update the state in the Store(s). The Dispatcher on the way delegates the Actions to the Store(s). The new state would be propagated from the Store(s) to the View to update them. The last part closes the loop of the unidirectional data flow.

The data flow goes in one direction. A View can trigger an Action, that goes through the Dispatcher and Store, and would change the View eventually when the state in the Store changed. The unidirectional data flow is enclosed in this loop. Then again, a View can trigger another Action. Since Facebook introduced the Flux architecture, the View was associated with React and its components.

You can [read more about the Flux architecture on the official website](https://facebook.github.io/flux/). There you will find a [video about its introduction at a conference](https://youtu.be/nYkdrAPrdcw?list=PLb0IAmt7-GS188xDYE-u1ShQmFFGbrk0v) too. If you are interested about the origins of Redux, I highly recommend reading and watching the material. After all, Redux became the successor library of the Flux architecture. Even though there were a bunch of solutions around the Flux architecture, Redux managed to surpass them. But why did it succeed?

[Dan Abramov](https://twitter.com/dan_abramov) and [Andrew Clark](https://twitter.com/acdlite) are the creators of Redux. It was [introduced by Dan Abramov at React Europe](https://www.youtube.com/watch?v=xsSnOQynTHs) in 2015. However, the talk by Dan doesn't introduce Redux per se. Instead, the talk introduced a problem that Dan Abramov faced that led to implementing Redux. I don't want to foreclose the content of the talk, that's why I encourage you to watch the video yourself. If you are keen to learn Redux, you should dive into the problem that was solved by it.

Nevertheless, one year later, again at React Europe, Dan Abramov reflected on the journey of Redux and its success. He mentioned a few things that had made Redux successful in his opinion. First, Redux was developed to solve a problem. The problem was explained by Dan Abramov one year earlier when he introduced Redux. It was not yet another library. It was a library that solved a problem. Time Traveling and Hot Reloading were the stress test for Redux. Second, the constraints of Redux were another key factor to its success. Redux managed to shield away the problem with a simple API and a thoughtful way to solve the problem of state management itself. You can [watch this talk](https://www.youtube.com/watch?v=uvAXVMwHJXU) too. I highly recommend it. Either you watch it right now or after the next chapter that introduces you to the basics of Redux.