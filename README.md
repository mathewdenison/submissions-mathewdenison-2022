## Getting Started

Clone this repo locally

Make a branch of this code and name the branch submissions/your-name-2022

Make commits to your branch as you would professionally 

(hint: make small commits with descriptive commit messages)

- make sure to install node js and yarn package manager on your computer
- from the application directory run the following commands in terminal

```
yarn install
yarn serve
```

You should see this output in your terminal after running `yarn serve`
```
code-test-2022~(main|✔) % yarn serve
yarn run v1.22.19
$ vue-cli-service serve
 INFO  Starting development server...


 DONE  Compiled successfully in 1602ms                                                                                                                                                            11:15:51 PM


  App running at:
  - Local:   http://localhost:8080/
  - Network: http://192.168.1.246:8080/

  Note that the development build is not optimized.
  To create a production build, run yarn build.
```

now you can navigate to http://localhost:8080 in your browser to see the working app.

This is a news feed app.

Your assignment:
1. **Replace** the article in `./src/App.vue` with a component. See `./src/components/HelloWorld.vue` for an example of a component and `./src/App.vue` for an example on how to consume. You may choose to refactor the HTML in the component to use `div`s instead of a table to organize HTML elements.
2. In `./src/App.vue` loop through the array of articles in `./assets/data.json` to render components with values from the array.
3. Style the Article component with the following using CSS:
   1. Title should have a yellow background
   2. text should be italicized
   3. article image should have rounded corners
   4. The article image should alternate from left to right (view the example screen shot ./public/Screenshot-example.png)


There is no time limit for this assessment.

Use as many outside resources as you need.

This is not a test of technical ability, but a test of how quickly you can pick up new languages, workflows, and skills. Do your best. Before submitting, make sure it compiles and runs.
