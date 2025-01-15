# vsc-catspeak

A VSCode extension that provides syntax highlighting for Catspeak. Also works in Markdown code fences (for Rusted Moss Mod Loader syntax). Only tested with the Night Owl theme, and personalized to my tastes, specifically. Feel free to modify it though.

If you want cool icons, download them from the Catspeak repository and add them as `icons/catspeak-logo-dark.svg` and `icons/catspeak-logo-light.svg`.

# To Install

Download a release over on the right and extract it in into somewhere safe (probably `[user home]/.vscode/extensions`). Then, use the `Developer: Install extension from location" command palette option to install it.

On Windows, this is `%USERPROFILE%/.vscode/extensions`. Linux is probably `~/.vscode/extensions`.

# To run locally (for testing purposes)

- Go to `Run -> Start Debugging` and select `Extension` to run the extension without installing.

# Test

```meow
-- this is some test catspeak for sanity checking
-- github has no idea what this is so don't expect highlighting here
self.transform_foreign_manifest = fun () {
  let names = struct_get_names(self.foreign_manifest)
  array_sort(names, true)
  self.foreign_manifest_list = []
  let j = 0
  while j < array_length(names) {
    let mod_name = names[j]
    let meta = self.foreign_manifest[mod_name]
    let local = self.local_manifest[mod_name]
    if local {
      meta._local = local.version
    }
    array_push(self.foreign_manifest_list, meta)
    j += 1
  }
}
```
