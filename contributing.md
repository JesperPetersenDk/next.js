# Contributing to Next.js

Our Commitment to Open Source can be found [here](https://zeit.co/blog/oss)

1. [Fork](https://help.github.com/articles/fork-a-repo/) this repository to your own GitHub account and then [clone](https://help.github.com/articles/cloning-a-repository/) it to your local device.
2. Install the dependencies: `npm install`
3. Run `npm run bootstrap`, which will link all repositories locally
4. Run `npm run dev` to build and watch for code changes

### To run tests

Running all tests:

```
yarn testonly
```

Running a specific test suite inside of the `test/integration` directory:

```
yarn testonly --testPathPattern "production"
```

Running just one test in the `production` test suite:

```
yarn testonly --testPathPattern "production" -t "should allow etag header support"
```

### Running the integration test apps without running tests

```
./node_modules/.bin/next ./test/integration/basic
```

### Testing in your own app

You only have to link the package once:

```
cd packages/next
```

```
npm link
```


Then link the `next` package inside your app:

```
npm link next
```

Then you can run your app with the local version of Next.js (You may need to re-run the example app as you change server side code in the Next.js repository).
