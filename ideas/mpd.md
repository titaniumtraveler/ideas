# Music Player Daemon

## Idea: Dynamic configuration

- propose set of commands to
  - set config item
  - get config item
  - read in file?
  - reset to file?
    - is there an obvious good behavior that could be happening there?
  - `version` to get full list of compiled features and daemon version
- security concept
  - new security scope, which is disabled by default
    - (As it is pretty easy to fuck things up with this!)
  - idea of service that proxies accesses and validates identity
  - Could also be done as just `ssh` with forwarding ...
- [[#Idea: Machine readable docs]]

## Idea: Machine readable docs

- Please have a *Machine readable* documentation
  - for config
  - for protocol commands
- Maybe could be generated from C headers?
- Would require some playing around with the build-system

## Todo: Document MPD on android

- Default config path?
- What socket-types are even supported?
- Extern data
- Blog Post?!
  - adb stuff
    - official docs
    - installation process
    - what files etc
    - workflow
      - (script to copy files and stuff)
- See the discussion at <https://github.com/MusicPlayerDaemon/MPD/discussions/2197>

## Todo: `mpc prio`

- It is just straight up missing from the docs ...
- Might look into writing them myself as part of
  [[#Idea: Machine readable docs]] ...

## Idea: `mpc socket`

- just use `mpc` to connect socket and give it to stdio ...
- a lot more convenient than `nc`, or `socat`

---

## Idea: Binary protocol for mpd??

- rather have a cool binary protocol than implementing http or something
  - rpc style?
- than that could be proxied to http
