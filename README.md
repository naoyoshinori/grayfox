grayfox
====

Simple VIM plugin manager.

## Usage

```
grayfox <command> <arguments...> [options...]
```

### Command

Installing and removing plugins.

```
grayfox install <plugin>
grayfox uninstall <plugin>
```

Create and delete profiles.

```
grayfox create <profile>
grayfox remove <profile>
```

Enable and disable the plugin.

```
grayfox use <profile>
grayfox enable <plugin> [-p|--profile] [--load-type]
grayfox disable <plugin> [-p|--profile] [--load-type]
```

## Example

Install the plugin. The plugin install location is `~/.vim/plugins/`

```
grayfox install 'altercation/vim-colors-solarized'
```

Uninstall the plugin.

```
grayfox uninstall 'altercation/vim-colors-solarized'
```

Create my profile. The profile localtion is `~/.vim/profiles/<profile>`

```
grayfox create MyProfile1
```

Use the created profile. Create a link in `~/.vim/pack/profile`.

```
grayfox use MyProfile1
```

Remove the profile.

```
grayfox remove MyProfile1
```

Enable plugin. Create a link in `~/.vim/pack/profile/start/<plugin>` or `~/.vim/pack/profile/opt/<plugin>`.

```
grayfox enable 'altercation/vim-colors-solarized'
```

You can specify a profile when plug-in is active.

```
grayfox enable 'altercation/vim-colors-solarized' -p MyProfile2
```

When loading the optional plugin please use the `--load-type` option. Create a link in `~/.vim/pack/profile/opt/<plugin>`.
The default is auto loading.

```
grayfox enable 'altercation/vim-colors-solarized' --load-type opt
```

Disable the plugin. Delete a link `~/.vim/pack/profile/start/<plugin>` or `~/.vim/pack/profile/opt/<plugin>`.

```
grayfox disable 'altercation/vim-colors-solarized'
```

## Install

```
git clone https://github.com/yoshi-naoyuki/grayfox.git
cd ./grayfox
cp grayfox /usr/local/bin/grayfox
```

## Licence

[MIT](https://github.com/yoshi-naoyuki/grayfox/blob/master/LICENSE)

## Author

[yoshi-naoyuki](https://github.com/yoshi-naoyuki)
