# Setting Details

All the following attributes serve various functions as how the collection/playlist functions inside of Plex Meta Manager.

| Attribute               | Description & Values                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name`                  | Used to specify the name off the collection/playlist in Plex as different then the mapping name.<hr>**Values:** Any String                                                                                                                                                                                                                                                                 |
| `template`              | Used to specify a template and template variables to use for this collection/playlist. See the [Templates Page](../templates) for more information.<hr>**Values:** Dictionary                                                                                                                                                                                                              |
| `run_again`             | Used to try and add all the missing items to the collection/playlist again after the daily run.<hr>**Values:** `true` or `false`<hr>**Default:** `false`                                                                                                                                                                                                                                   |
| `sync_mode`             | Used to change how builders sync with this collection/playlist.<hr>**Values:**<table class="clearTable"><tbody><tr><td>`append`</td><td>Only Add Items to the Collection</td></tr><tr><td>`sync`</td><td>Add & Remove Items from the Collection</td></tr></tbody></table><hr>**Default:** [settings library value](../../config/settings)                                                  |
| `minimum_items`         | Minimum items that must be found to add to a collection/playlist.<hr>**Values:** number greater then 0<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                     |
| `delete_below_minimum`  | Deletes the collection/playlist if below the minimum.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                     |
| `delete_not_scheduled`  | Deletes the collection/playlist if its skipped because its not scheduled.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                 |
| `validate_builders`     | When set to false the collection/playlist will not fail if one builder fails.<hr>**Values:** `true` or `false`<hr>**Default:** `true`                                                                                                                                                                                                                                                      |
| `build_collection`      | When set to false the collection won't be created but items can still be added to Radarr/Sonarr. Does not work for playlists.<hr>**Values:** `true` or `false`<hr>**Default:** `true`                                                                                                                                                                                                      |
| `server_preroll`        | Used to set the `Movie pre-roll video` Text box in Plex under Settings -> Extras.<br>You can run this with a [schedule](schedule) to change the pre-rolls automatically.<hr>**Values:** Any String                                                                                                                                                                                         |
| `missing_only_released` | Collection/Playlist Level `missing_only_released` toggle.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                 |
| `only_filter_missing`   | Collection/Playlist Level `only_filter_missing` toggle.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                   |
| `show_filtered`         | Collection/Playlist level `show_filtered` toggle.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                         |
| `show_missing`          | Collection/Playlist level `show_missing` toggle.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                          |
| `save_missing`          | Collection/Playlist level `save_missing` toggle.<hr>**Values:** `true` or `false`<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                                                                                                          |
| `ignore_ids`            | Collection/Playlist level `ignore_ids` which is combined with the library and global `ignore_ids`.<hr>**Values:** List or comma-separated String of TMDb/TVDb IDs<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                          |
| `ignore_imdb_ids`       | Collection/Playlist level `ignore_imdb_ids` which is combined with the library and global `ignore_imdb_ids`.<hr>**Values:** List or comma-separated String of IMDb IDs<hr>**Default:** [settings library value](../../config/settings)                                                                                                                                                     |
| `name_mapping`          | Used to specify the folder name in the [Image Assets Directory](../../home/guides/assets) i.e. if your collection/playlist name contains characters that are not allowed in file paths (i.e. for windows `<`, `>`, `:`, `"`, `/`, `\`, `?`, `*` cannot be in the file path), but you want them in your name you can this to specify the name in the file system.<hr>**Values:** Any String |
| `test`                  | When running in Test Mode (`--run-tests` [option](../../home/environmental)) only collections/playlists with `test: true` will be run.<hr>**Values:** `true` or `false`<hr>**Default:** `false`                                                                                                                                                                                            |
| `changes_webhooks`      | Used to specify a collection/playlist changes webhook for just this collection/playlist.<hr>**Values:** List of webhooks                                                                                                                                                                                                                                                                   |
