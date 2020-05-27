# `git-timestamp`
Boilerplate repository for RFC3161 TSA Git repository commit timestamping.

## Requirements

* `coreutils`
* `openssl`
* `curl`

## Install

1. Copy the [`./timestamp`](./timestamp) directory to the root of your repository.

2. Set up Git to use the included hook scripts:

    ```bash
    git config --local core.hooksPath timestamp/hooks
    ```
    
3. Create a test commit and check the [`timestamp`](./timestamp) directory.

## Settings

You can choose which timestamping authority servers to use by editing [`./timestamp/servers.list`](./timestamp/servers.list) file.

## Persistence

The hooks won't remain enabled across devices, so you'll need to run the `git config` command each time you clone the repository to a new device.
