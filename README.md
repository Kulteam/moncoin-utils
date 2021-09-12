
# MONCoin Javascript Utilities

[![NPM](https://nodei.co/npm/moncoin-utils.png?downloads=true&stars=true)](https://nodei.co/npm/moncoin-utils/)

This package contains code that wraps [moncoin-crypto](https://github.com/Kulteam/moncoin-crypto) primitives into an easier to use interface. This includes the ability to easily discover funds for a wallet, create transactions, sign transactions (ring signatures), create new wallets, verify addresses, and handful of other useful methods. These methods can then be wrapped into a Javascript-based wallet such as [moncoin-wallet-backend-js](https://github.com/Kulteam/moncoin-wallet-backend-js).

If you experience any issues with this library, the best way to address such situations is to submit a Pull Request to resolve the issue you are running into.

## Installation

```bash
npm install moncoin-utils
```

## Initialization

### JavaScript

```javascript
const MONCoinUtils = require('moncoin-utils').CryptoNote
const coinUtils = new MONCoinUtils()
```

### TypeScript

```typescript
import { CryptoNote } from 'moncoin-utils'
const coinUtils = new CryptoNote()
```

You can find TypeScript type definitions [here](index.d.ts)

### Browser Support

When packing for the browser with a tool like [webpack](https://webpack.js.org/) we advise that you use the ready `event` of the webpacked module to determine when the Cryptographic methods are available.

```html
<script src="MONCoinUtils.js"></script>
<script>
  MONCoinUtils.on('ready', () => {
    const coinUtils = new MONCoinUtils.CryptoNote()
  })
</script>
```

### Documentation

You can find the full documentation for this library [here](https://moncoin.io)

### Credits

Special thanks goes out to:

* Lucas Jones
* Paul Shapiro
* Luigi111
* [The MyMonero Project](https://github.com/mymonero/mymonero-app-js)
* The Masari Project: [gnock](https://github.com/gnock)
* The Plentum Project: [DaveLong](https://github.com/DaveLong)
