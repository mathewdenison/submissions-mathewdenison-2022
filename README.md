## Getting Started

- make sure to install node js and yarn package manager on your computer
- from this directory run the following commands

```
yarn install
yarn serve
```

you should see this output in your terminal after running `yarn serve`
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

Your assignment is to build a reusable component to **replace** each article in `./src/App.vue`. You should not use the table format in the example article.

You will need to loop through the data array of articles to populate your component for each article. There is an example of a component in `./src/components/HelloWorld.vue`

Each Article title should have a yellow highlighted background and the text should be italicized. The article image should have rounded corners and every other article the image should be on the opposite side. This should be done with CSS.