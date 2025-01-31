# Vegetable Oil

CLI Tool for [`oil`]-like transformations

- json with current state of directories and files
- transforms based on that

- commands
  - `read() -> Result<State>`
    - read current file state
    - `-r` recursive
  - `check(current: State) -> Option<State>`
    - like read, but confirms that filesystem is `current`
    - `-d` diff rather than check
    - returns `Actions` of `current` filesystem state
  - `diff(current, next) -> Vec<Action>`
    - give diff between `current` and `next`
  - `execute(current, next) -> Result<()>`
    - perform the steps needed to achieve `next`

- types
  - State
    - description of the state of a bunch of files
  - Entry
    - id   - unique identifier of file
    - path - path of entry
    - type - type of entry: file, directory, symlink, hardlink
  - Action
    - keep
    - move
    - copy
    - remove
    - create symlink
    - create hardlink

    - later special things like
      - chmod
      - time

- limitations
  - only support linux for now
  - add an `Backend` trait later
  - only utf-8 paths are supported for now
    - mostly because json doesn't encode `u8`s well
      (I could represent them as base64 tho ...)

[`oil`]: https://github.com/stevearc/oil.nvim
