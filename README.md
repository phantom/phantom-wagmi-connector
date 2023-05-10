# Phantom Wagmi Connector
This small package allows you to add a dedicated, functional, connector to integrate Phantom into your wagmi ^v1 project

to install
```sh
yarn add phantom-wagmi-connector
# or
npm install phantom-wagmi-connector
# or
pnpm add phantom-wagmi-connector
```

## Import
```javascript
import { PhantomConnector } from 'phantom-wagmi-connector'
```

## Usage
```javascript
import { PhantomConnector } from 'phantom-wagmi-connector'

const connector = new PhantomConnector()
```

## Configuration

### chains (optional)
```javascript
import { mainnet, polygon } from 'wagmi/chains'
import { PhantomConnector } from 'phantom-wagmi-connector'

const connector = new PhantomConnector({
  chains: [mainnet, polygon],
})
```
### options (optional)
Options for configuring the connector.

```javascript
import { PhantomConnector } from 'phantom-wagmi-connector'
 
const connector = new PhantomConnector({
  options: {
    shimDisconnect: true,
  },
})
```

### shimDisconnect

Phantom does not support programmatic disconnect on EVM chains. This flag simulates the disconnect behavior by keeping track of connection status in storage. Defaults to true.
```javascript

import { PhantomConnector } from 'phantom-wagmi-connector'
 
const connector = new PhantomConnector({
  options: {
    shimDisconnect: false,
  },
})
```