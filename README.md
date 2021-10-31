# Remix-Firebase

## Development

You'll need to run three terminals (or bring in a process manager like concurrently/pm2-dev if you like):

Start the Remix development asset server

```sh
npm run dev
```

In a new tab start functions TypeScript compiler:

```sh
npm run dev:functions
```

In a new tab start Firebase emulators:

```sh
npm run start
```

## Deployment

First, build your Remix app for production:

```sh
npm run build
```

Second, build Cloud Functions:

```sh
npm run build:functions
```

Then deploy your Cloud Functions and Hosting (this runs the functions build script as well)
```sh
firebase deploy --only hosting,functions:remix
```