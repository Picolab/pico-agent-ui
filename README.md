# pico-agent-ui
standalone UI for a Pico Agent

For those conversant with picos, the usual UI for a pico includes an Agent tab.

For those uninterested in other pico operations, or unable to use the usual UI,
it will be useful<sup>*</sup> to have a standalone UI to operate a Pico Agent.

The operator of the pico-engine which hosts picos will need to install in its `public` folder
the file named `agent.html` developed in this repository.

A pico-engine can be installed from [the pico-engine repository](https://github.com/Picolab/pico-engine).

The rulesets that need to be installed in a pico so that it becomes a Pico Agent can be registered from
[the G2S repository](https://github.com/Picolab/G2S).
The same repository also contains rulesets which can be used to deploy and operate an agency.
An agency can be used to create and host a new Pico Agent.

If you are running an Agency, you can place the file `agent.html` in your pico-engine `public` folder.
Then you can instruct your clients, instead of logging in, to use their DID in a URI like this one,
replacing "HOST" and "PORT" with your pico-engine host and port,
and "DID" with their DID.

```
https://HOST:PORT/agent.html#DID
```
<sup>*</sup> A pico-engine used to host an agency SHOULD be run using `https`
(typically by setting up an `nginx` server that reverse proxies to the pico-engine).
In this case, the regular pico-engine UI SHOULD NOT be accessible to anyone other 
than a system administrator.
This is done by requiring a password for all of the `/api` routes into the pico-engine.

