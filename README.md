
### Installation

```
npm install --save orderlock
```

### Usage

!-- Proposed Interface --!

```

import orderlock from 'orderlock'

async function main() {

  const lock: orderlock.Lock = await orderlock.getLock({
    location: /* RUN Location of OrderLock Instance */
  })

  const transaction: orderlock.Transaction = await lock.unlock({
    privateKey: process.env.bsv_private_key,
    utxos: [/* optionally include the explicit coins to spent */],
    transmit: false /* when true broadcasts the transaction */
  })

}

```

### Building

```
npm run build
```
