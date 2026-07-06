# compositor-support

This repository contains information about Wayland compositors and the globals
that they support. The per-compositor information is stored in the data
directory.

If you are a compositor developer or can get a developer to sign off on it, you

- can be added as a collaborator to this repository,
- can be added to the CODEOWNERS file.

This will allow you to merge pull requests modifying your compositor's JSON
file.

## Generating the JSON file

The JSON files are generated using [wlprobe]. You can invoke it as follows:

```shell
~$ wlprobe --unique
{
  "generationTimestamp": 1783520564773,
  "globals": [
    {
      "interface": "ext_foreign_toplevel_image_capture_source_manager_v1",
      "version": 1
    },
...
```

You need to manually add the top-level `version` field which should contain the
version of the compositor.

[wlprobe]: https://github.com/PolyMeilex/wlprobe

## License

[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)
