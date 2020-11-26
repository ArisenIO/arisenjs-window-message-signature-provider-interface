# ARISEN Signature Provider for Desktop Browsers

A [Signature Provider Interface](https://github.com/ARISENIO/arisen-signature-provider-interface) for communicating with an authenticator over the [Window Messaging API](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) using the [ARISEN Authentication Transport Protocol Specification](https://github.com/ARISENIO/arisen-authentication-transport-protocol-spec).

## Overview

When plugged into `ARISENJS`, this signature provider enables desktop web applications to route signing requests to a browser extension authenticator. Full instructions for `ARISEN` can be found [here](https://github.com/arisenio/arisenjsv1).

## Installation

```bash
yarn add arisenjs-window-message-signature-provider-interface
```

## Basic Usage

```javascript
import { Api, JsonRpc } from "ARISEN"
import { SignatureProvider } from "arisenjs-window-message-signature-provider-interface"

const rpc = new JsonRpc("RPC_ENDPOINT_HERE")
const signatureProvider = new SignatureProvider({
  declaredDomain: "YOUR_DOMAIN", // This domain must have a `chain-manifests.json` file at the root
  returnUrl: "YOUR_DOMAIN",
})
const api = new Api({
  rpc,
  signatureProvider,
})

api.transact(...)

```

## Links
- [Signature Provider Interface](https://github.com/ARISENIO/arisen-signature-provider-interface)
- [Window Messaging API](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage)
- [ARISEN Authentication Transport Protocol Specification](https://github.com/ARISENIO/arisen-authentication-transport-protocol-spec)

## Contribution
Check out the [Contributing](./CONTRIBUTING.md) guide and please adhere to the [Code of Conduct](./CONTRIBUTING.md#conduct)

## License
[MIT licensed](./LICENSE)

## Important

See LICENSE for copyright and license terms.  Arisen makes its contribution on a voluntary basis as a member of the ARISEN community and is not responsible for ensuring the overall performance of the software or any related applications.  We make no representation, warranty, guarantee or undertaking in respect of the software or any related documentation, whether expressed or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall we be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or documentation or the use or other dealings in the software or documentation. Any test results or performance figures are indicative and will not reflect performance under all conditions.  Any reference to any third party or third-party product, service or other resource is not an endorsement or recommendation by Arisen.  We are not responsible, and disclaim any and all responsibility and liability, for your use of or reliance on any of these resources. Third-party resources may be updated, changed or terminated at any time, so the information here may be out of date or inaccurate.  Any person using or offering this software in connection with providing software, goods or services to third parties shall advise such third parties of these license terms, disclaimers and exclusions of liability.  Arisen, ARISEN, ARISEN Labs, ARISEN, the heptahedron and associated logos are trademarks of Arisen.

Wallets and related components are complex software that require the highest levels of security.  If incorrectly built or used, they may compromise users’ private keys and digital assets. Wallet applications and related components should undergo thorough security evaluations before being used.  Only experienced developers should work with this software.
