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

**Today's Progress**: Adder the example 9 from the book
This example adds an end-to-end test and show an example of middleware using the httprouter and negroni packages.
