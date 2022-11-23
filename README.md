# AesirX DAM

## About

AesirX DAM is our Open-Source PWA-powered enterprise-level Digital Asset Management as a Service (DAMaaS) Solution

Find out more in [https://dam.aesirx.io](https://dam.aesirx.io)

## Development setup

### Configure

1. Get your `REACT_APP_CLIENT_SECRET` key from https://dam.aesirx.io by creating an account.
1. Rename the `.env.dist` file to `.env`.
1. Replace the `REACT_APP_CLIENT_SECRET` in the `.env` file with the one provided in your profile account.

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### `npm build`

Get a full build and install it in your favorite web server.


## Integrate setup

The easiest way to use aesirx-dam-app is to install it from npm and build it into your app with Webpack.

```
npm install aesirx-dam-app
```

Then use it in your app:

```js
import React, { useState } from 'react';

import { AesirXDam } from 'aesirx-dam-app';

import 'aesirx-dam-app/dist/index.css';
import 'aesirx-dam-app/dist/index.css.map';

function AesirXDam() {
  const [show, setShow] = useState(true);
  const onDoubleClick = (data) => {
    // do something when user onDoubleClick at on that assets
  };
  const onShow = () => {
    // on Show
  };
  const onHide = () => {
    // on Hide
  };
  return (
    <div className="py-4 px-3 h-100 flex-direction-column">
      <div className="h-100 flex-1">
        <AesirXDam show={show} onShow={onShow} onHide={onHide} onDoubleClick={onDoubleClick} />
      </div>
    </div>
  );
}

export default AesirXDam;

```

## Props

Common props you may want to specify include:

- `modalClassname` - apply a className to modal
- `contentClassName` - apply a className to modal content
- `bodyClassName` - apply a className to modal body
- `dialogClassName` - apply a className to modal dialog
- `show` - show the modal when it true
- `onHide` - subscribe to hide event
- `onShow` - subscribe to show event
