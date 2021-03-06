# 100 Days Of Code - Log

### Day 0: January 02, 2017

**Today's Progress**: Created repos to develop the examples of "Building Web Apps with Go" codegangsta's book, added the book's first example a file server written in go. [Repo](https://github.com/andredurao/building-web-apps-with-go.git)

**Thoughts:** This is my first day, so I'll keep up reading the book and implementing the examples

**Link to work:** [Book1](https://www.gitbook.com/book/astaxie/build-web-application-with-golang/details)
**Link to work:** [Book2](https://www.gitbook.com/book/codegangsta/building-web-apps-with-go/details)


### Day 1: January 03, 2017

**Today's Progress**: Added the log interface on the first example and the second example from the book

**Thoughts** I should also add the same log interface that I've added on the first example on the second.


### Day 2: January 04, 2017

**Today's Progress**: Continued with the second example from the book and tried to deploy the Markdown app to heroku.
It didn't worked YET, though the book explanation was easy the Heroku deploy was rejected:

```
  error fetching custom buildpack
```

I've decided to follow Heroku's documentation on how to deploy go applications (https://devcenter.heroku.com/articles/getting-started-with-go) and deploy the Markdown example based on that.

I've also created a new repository (https://github.com/andredurao/simple-markdown-generator-in-go) where I will follow the Heroku's documentation and deploy the app.

**Thoughts** The sample app from Heroku was deployed to https://frozen-depths-34486.herokuapp.com/

### Day 3: January 05, 2017

**Today's Progress**: Did a lot of changes on the second example.
1. Learned about govendor (https://github.com/kardianos/govendor) and gin (https://github.com/gin-gonic/gin).
2. I've replaced the original index.html from the example into three templates index, header and footer.
3. Used the govendor to maintain the dependecies on my app.
4. Created a get function for gin router's to serve the main content
5. Created a post function to generate the html from the markdown

### Day 4: January 06, 2017

**Today's Progress**: Finally deployed the app on heroku.
The app is at (https://simplemarkdowngenerator.herokuapp.com/) and it follows the style and structure of Heroku's example.
1. `heroku local` was running a different app because I forgot to update the `Procfile` with the name of the project
2. To run `heroku local` I needed to compile and install the binaries of the project `go build` and `go install`
3. Another thing that is different from the book: the buildpack informed is no longer a github repository; now it's just `heroku/go`
4. Now I can continue with the book.

### Day 5: January 07, 2017

**Today's Progress**: Added example 3 from the book.
Also added a README, which by the way I think it should be present on all examples, on example 3.

### Day 6: January 08, 2017

**Today's Progress**: Added example 4 from the book.
Also added a README, This example is just to explain how a middleware is implemented. It is not safe to add the password on a parameter via GET, OK. But instead of a password check this middleware could check a cookie to verify if a user is logged on the app.

### Day 7: January 09, 2017

**Today's Progress**: Added the example 5 from the book.
This example, although simpler the the fourth, covers two Go concepts: Structs and Encodings

### Day 8: January 10, 2017

**Today's Progress**: Added the example 6 from the book.
This example, uses the template interface from golang. I'm thinking that I will need to update the directory structure to group the rendering examples on a same directory.

### Day 9: January 11, 2017

**Today's Progress**: Added the example 7 from the book.
This example shows a simple usage of `render` package and how it can help rendering different types of content.

### Day 10: January 12, 2017

**Today's Progress**: Added the example 8 from the book.
This example loads a simple server and testes if the param custom_param is on the response on a test

### Day 11: January 13, 2017

**Today's Progress**: Added the example 9 from the book
This example adds an end-to-end test and show an example of middleware using the httprouter and negroni packages.

### Day 12: January 14, 2017

**Today's Progress**: Added the example 10 from the book
This example took was the most difficult because it required the understanding of almost all the previous examples.
I've managed to implement the exercises; Now I need to check how good they are written.

### Day 13: January 15, 2017

**Today's Progress**: Added the example 11 from the book
This example was missing some information about how to insert data on books table, I've added how I did on the README file.
I've managed to implement the exercises; Now I need to check how good they are written.

### Day 14: January 16, 2017

**Today's Progress**: Implementing the query records exercise fom databases chapter
Created the struct Book and now I'm trying to load all records of books on a `map` of Book.
It's not running, yet. Hopefully I will finish this exercise tomorrow.

### Day 15: January 17, 2017

**Today's Progress**: Iterating through the Books map array.
Prepared the action to fill a map of Book structs.
Next step: iterate and render the map on the view(template)

### Day 16: January 18, 2017

**Today's Progress**: Iterating through the Books map array.
Created a template and moved the iteration to the view: OK!

### Day 17: January 19, 2017

**Today's Progress**: Created a Dockerfiler to learn how to run apps like this on Docker.
Followed these guides, but there's still much to learn:

https://blog.golang.org/docker
https://blog.codeship.com/what-is-a-dockerfile/
https://blog.codeship.com/building-minimal-docker-containers-for-go-applications/

### Day 18: January 20, 2017

**Today's Progress**: I was looking for a way to check the temperature of my mac and most of the things I found required an app to be installed.
I wish to do that on a command line, not to install some app that bundles a lot of others things that may not be useful to me.
Then I found this ruby gem (iStats) that gives me that data, the gem comes with a fancy executable with shows some graphs on the terminal.
It's ok that's what I want. After a look at the native extension I've decided to change a few things because there's no need for a Gem for what I need.

I've created this repository on https://github.com/andredurao/osx-cpu-info which contains the iStats gem native functions without the ruby bindings.

### Day 19: January 21, 2017

**Today's Progress**: Got back on golang, now implementing and studying astaxie's book.

### Day 20: January 22, 2017

**Today's Progress**: Arranged the directories to split examples from codegangsta and astaxie books.
Also added the second example from astaxie's book.

### Day 21: January 23, 2017

**Today's Progress**: Added the third example from astaxie's book (http forms)

### Day 22: January 24, 2017

**Today's Progress**: Back on cpu-info C project; I've added a main file to parse arguments.
My goal is to split the main and lib files to get a lightweight executable that's usable even on PS1(prompt) or undex TMUX status bar

### Day 23: January 25, 2017

**Today's Progress**: Took out the debug to another function and added the osx-cpu-info.c file on main.
Next step: call the lib functions on the main file.

### Day 24: January 27, 2017

**Today's Progress** Added the example 04 from astaxies's book:processing form inputs

### Day 25: January 30, 2017

**Today's Progress** Changed a few items on cpu-info-app

### Day 26: January 31, 2017

**Today's Progress** Added a string on cpu-info-app that will be used to concatenate all info on it

### Day 27: February 01, 2017

**Today's Progress** Dinamically allocated the memory (maloc) for infoString and used it via `strncat`

### Day 28: February 06, 2017

**Today's Progress** Added battery temperature function and option via getopt

### Day 29: February 07, 2017

**Today's Progress** Added battery health option and a important FIXME that changes the program behaviour

### Day 30: February 08, 2017

**Today's Progress** Added battery cycle count function, but it's returning 1000. Now I need to check if that value is correct

### Day 31: February 10, 2017

**Today's Progress** Added battery time remaining function

### Day 32: February 11, 2017

**Today's Progress** Added fan speed function
