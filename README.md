 
# Consumer App for my-node-module

A simple consumer app to demonstrate the usage of the `my-node-module` Node package.

## Table of Contents

1. [File Structure](#file-structure)
2. [Install and Run](#install-and-run)
3. [Linking my-node-module Locally](#linking-my-node-module-locally)

## File Structure

```
my-consumer-app/
|-- node_modules/
|-- package.json
|-- index.js
```

## Contents of Each File

### 1. `package.json`

```json
{
  "name": "my-consumer-app",
  "version": "1.0.0",
  "description": "Consumer app for my-node-module",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "my-node-module": "^1.0.0"
  }
}
```

### 2. `index.js`

```javascript
// index.js
const helloWorld = require('my-node-module');

console.log(helloWorld());
```

## Install and Run

1. Navigate to the `my-consumer-app` directory:

   ```bash
   cd path/to/my-consumer-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the app:

   ```bash
   npm start
   ```

   Check the console output to see the result.

## Linking my-node-module Locally

If you're making changes to `my-node-module` and want to test it locally in `my-consumer-app` without publishing it to npm:

1. Navigate to the `my-node-module` directory:

   ```bash
   cd path/to/my-node-module
   ```

2. Link the module locally:

   ```bash
   npm link
   ```

3. Navigate back to the `my-consumer-app` directory:

   ```bash
   cd path/to/my-consumer-app
   ```

4. Link `my-node-module` in `my-consumer-app`:

   ```bash
   npm link my-node-module
   ```

   This creates a symbolic link between the two projects.

5. Run the app:

   ```bash
   npm start
   ```

   Now, any changes made to `my-node-module` will be reflected in `my-consumer-app`.
 