# EOS Resources

Quickly and easily retrieve EOS Resources metrics from the EOSIO blockchain.

> This library is being actively maintained by [EOS Nation FTW](https://eosnation.io), show your support by voting for `eosnationftw` on the EOSIO mainnet.

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [eosRamPriceKb](#eosrampricekb)
    -   [Parameters](#parameters)
    -   [Examples](#examples)
-   [eosCpuPriceMs](#eoscpupricems)
    -   [Parameters](#parameters-1)
    -   [Examples](#examples-1)
-   [eosNetPriceKb](#eosnetpricekb)
    -   [Parameters](#parameters-2)
    -   [Examples](#examples-2)
-   [getAccount](#getaccount)
    -   [Parameters](#parameters-3)
    -   [Examples](#examples-3)
-   [getRAMMarket](#getrammarket)
    -   [Parameters](#parameters-4)
    -   [Examples](#examples-4)

### eosRamPriceKb

EOS RAM Price in kilobytes

#### Parameters

-   `rammarket` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)?** table eosio eosio rammarket (JSON)

#### Examples

```javascript
import { eosRamPriceKb } from 'eos-resources';

(async () => {
  const priceKb = await eosRamPriceKb(rammarket);
  priceKb //=> 0.08044544
})()
```

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)>** EOS RAM Price in kilobytes

### eosCpuPriceMs

EOS CPU Price in milliseconds

#### Parameters

-   `account` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)?** Account Details JSON

#### Examples

```javascript
import { eosCpuPriceMs } from 'eos-resources';

(async () => {
  const priceMs = await eosCpuPriceMs();
  priceMs //=> 26.415
})()
```

Returns **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** EOS CPU Price in milliseconds

### eosNetPriceKb

EOS Net Price in kilobytes

#### Parameters

-   `account` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)?** Account Details JSON

#### Examples

```javascript
import { eosNetPriceKb } from 'eos-resources';

(async () => {
  const priceKb = await eosNetPriceKb();
  priceKb //=> 607.375
})()
```

Returns **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** EOS Net Price in kilobytes

### getAccount

Get Account

#### Parameters

-   `account_name` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Account Name
-   `api` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** EOSIO API endpoint (optional, default `"https://api.eosn.io"`)

#### Examples

```javascript
import { getAccount } from 'eos-resources';

(async () => {
  const account = await getAccount('eosnationftw');
  account //=> EOSIO Account JSON
})()
```

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)>** Account Details JSON

### getRAMMarket

Get RAM Market

#### Parameters

-   `api` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** EOSIO API endpoint (optional, default `"https://api.eosn.io"`)

#### Examples

```javascript
import { getRAMMarket } from 'eos-resources';

(async () => {
  const rammarket = await getRAMMarket();
  rammarket //=> EOSIO RAM Market JSON
})()
```

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)>** RAM Market JSON
