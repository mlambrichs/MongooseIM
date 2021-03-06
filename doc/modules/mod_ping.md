### Module Description

This module implements XMPP Ping functionality as described in
[XEP-0199: XMPP Ping](http://www.xmpp.org/extensions/xep-0199.html).


### Options

* `send_pings` (boolean, default `false`): If set to true, the server will send ping iqs to the client if they are not active for `ping_interval`.
* `ping_interval` (seconds, default `60`): Defines the client inactivity timeout after which server will send ping request if above option is set to `true`.
* `timeout_action` (`none` | `kill`, default `none`): Defines if the client connection should be closed if it doesn't reply to ping request in less than `ping_req_timeout`.
* `ping_req_timeout` (seconds, default `32`) Defines how long the server waits for the client to reply to the ping request.
* *`iqdisc`

### Example Configuration

```
  {mod_ping, [{send_pings, true}]},
```
