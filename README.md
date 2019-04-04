# react-amplitude-without-webpack

# Fork from react-amplitude

### React Amplitude Analytics

## Usage

Initializing:

```js
import React from 'react';
import ReactDOM from 'react-dom';

...
import Amplitude from 'react-amplitude';
Amplitude.init('YOUR_UNIQUE_TRACKING_CODE');
...

document.addEventListener('DOMContentLoaded', function() {
  ReactDOM.render(<App />, document.getElementById('app'));
});

```

## API

#### Amplitude.init(apiKey, userId, config, callback)

Must be initialized using this function before any of the other tracking functions will record any data.

###### Example

```js
Amplitude.init(apiKey, userId, config, cb);
```

| Value    | Notes                 |
| -------- | --------------------- |
| apiKey   | `String`. Required.   |
| userId   | `String`. Optional.   |
| config   | `Object`. Optional.   |
| callback | `Function`. Optional. |

#### Amplitude.logEvent(eventName, eventProperties, callback)

Log an event to Amplitude.

###### Example

```js
Amplitude.logEvent(eventName, eventProperties, cb);
```

| Value           | Notes                 |
| --------------- | --------------------- |
| eventName       | `String`. Required.   |
| eventProperties | `Object`. Optional.   |
| callback        | `Function`. Optional. |

#### Amplitude.logEventWithTimestamp(eventName, eventProperties, timestamp, callback)

Log an event to Amplitude.

###### Example

```js
Amplitude.logEventWithTimestamp(eventName, eventProperties, timestamp, cb);
```

| Value           | Notes                 |
| --------------- | --------------------- |
| eventName       | `String`. Required.   |
| eventProperties | `Object`. Optional.   |
| timestamp       | `Number`. Optional.   |
| callback        | `Function`. Optional. |

#### Amplitude.resetUserId()

Remove user tracking (e.g. on logging out).

###### Example

```js
Amplitude.resetUserId();
```

#### Amplitude.setUserId(userId)

Track users through a unique user id.

###### Example

```js
Amplitude.setUserId(userId);
```

| Value  | Notes               |
| ------ | ------------------- |
| userId | `String`. Required. |

#### Amplitude.setUserProperties(userProps)

Track user properties

###### Example

```js
Amplitude.setUserProperties(userProps);
```

| Value     | Notes               |
| --------- | ------------------- |
| userProps | `object`. Required. |

#### Amplitude.clearUserProperties()

Clear user properties
(careful, this is irreversible!)

###### Example

```js
Amplitude.clearUserProperties();
```

#### Amplitude.getSessionId()

Returns current session id

###### Example

```js
Amplitude.getSessionId();
```

#### Amplitude.identify(idObj, callback)

Send an identify call containing user property operations to Amplitude servers

###### Example

```js
Amplitude.identify(idObj, cb);
```

| Value    | Notes                 |
| -------- | --------------------- |
| idObj    | `object`. Required.   |
| callback | `Function`. Optional. |

#### Amplitude.isNewSession()

Returns if a new session was created at init

###### Example

```js
Amplitude.isNewSession();
```
