# Setting Up Express Server

## Installation

```bash
npm install express body-parser cookie-parser compression cors
npm install --save-dev @types/express @types/body-parser @types/cookie-parser @types/compression @types/cors
```

## Importing Modules

Import the necessary modules in your server file:

```javascript
import express from 'express';
import http from 'http';
import bodyParser from 'body-parser';
import cookieParser from 'cookie-parser';
import compression from 'compression';
import cors from 'cors';
```
## Creating the Express App

Create an instance of the Express application and configure it with middleware:

```javascript
const app = express();

app.use(cors({
    credentials: true,
}));

app.use(compression());
app.use(cookieParser());
app.use(bodyParser.json());
```

## Creating the HTTP Server
Create an HTTP server using the Express app:

```javascript
const server = http.createServer(app);
```

````javascript
server.listen(8080, () => {
    console.log('Server is running on port 8080');
})
```

## Database Setup

Install Mongoose and add the database URL in the `index.ts` file:

```bash
npm install mongoose
npm install -D @types/mongoose
```
In your `index.ts` file, add the following code to connect to your database:

```typescript
const dbUrl = 'your-database-url-here';
```

```typescript
mongoose.Promise = Promise;
mongoose.connect(MONGO_URL);
mongoose.connection.on('error', (error: Error) => console.log(error));
mongoose.connection.on('open', () => console.log('Connected to MongoDB'));
```

Now in the src directory, create a folder db in that create a file users.ts and create users model

After creating the userModal, now create a directory within the src folder called helpers and index.ts file into it. This folder is for creating helpers for authentication

Latter create the authentication.ts file in the controllers directory of app directory

Next, create a directory routes and add 2 files index.ts and authentication.ts

now create middlewares before that go to terminal install lodash

## Installation

```bash
npm install lodash
npm install -D @types/lodash
```

After setting up the middleware, we have to go and create another controller named users.ts, then eventually add it to the router and wrap up irrevocably by getting users and some functionalities
