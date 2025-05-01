# superDirtSocket

Tiny thing to listen on a WebSocket and forward OSC-over-UDP events to SuperDirt

# How to use

## NPM

1. Install in an npm initialized project.

```sh
npm install @diegovdc/superdirt-socket
```

2. Run

```sh
npx superDirtSocket --superCollider 57120 -v
```

3. If you want to add custom superdirt args beyond the already registered.
   Create a file that defines the args:

```js
// ./customSuperDirtArgs.js
module.exports = { cc20: "i" };
```

Run this command:

```sh
npx superDirtSocket --superCollider 57120 -v --superDirtArgs ./customSuperDirtArgs.js
```

## Cloning

1. Clone it somewhere useful (just one-time):

```
cd ~
git clone https://github.com/Piraran/superDirtSocket.git
```

1. Install node.js, SuperCollider and SuperDirt (just one-time)

2. Install node modules used by this thing (just one-time):

```
cd ~/superDirtSocket
npm install
```

1. To make it go, run it with node:

```
cd ~/superDirtSocket
node superDirtSocket.js --superCollider 57120
```

1. Finally, launch SuperDirt, open a browser and connect to a running Estuary deployment somewhere. Check the SuperDirt checkbox at the top of Estuary to connect, through the superDirtSocket, to SuperDirt.
