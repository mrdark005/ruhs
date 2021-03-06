![ruhsImage](https://cdn.discordapp.com/attachments/751536546578038874/752087414805364736/ruhs_2.png)

# ruhs
A lightweight Discord library for Node.

[![npm dependencies](https://img.shields.io/librariesio/release/npm/ruhs?style=flat-square)](https://npmjs.com/package/ruhs?activeTab=dependencies)
[![npm version](https://img.shields.io/npm/v/ruhs?style=flat-square)](https://npmjs.com/package/ruhs)
[![npm downloads](https://img.shields.io/npm/dt/ruhs?style=flat-square)](https://npmjs.com/package/ruhs)
[![npm license](https://img.shields.io/npm/l/ruhs?style=flat-square)](https://npmjs.com/package/ruhs)
[![CodeFactor](https://img.shields.io/codefactor/grade/github/acarnd03/ruhs?style=flat-square)](https://codefactor.io/repository/github/acarnd03/ruhs)

[Website/Docs](https://acarnd03.gitbook.io/ruhs)

## Example code
```js
const ruhs = require("ruhs");
const token = "your token";

ruhs.eventHandlers.ready = (() => {
  // guilds aren't cached for now, wait ~1.5 second for be cached all guilds.
  setTimeout(() => {
    console.log(ruhs.cache.guilds);
  }, 1500);
});

ruhs.eventHandlers.messageCreate = ((message) => {
  console.log(message.content);
});

(async () => {
  await ruhs.createClient(token, {
    "intents": "ALL"
  });
})();
```
