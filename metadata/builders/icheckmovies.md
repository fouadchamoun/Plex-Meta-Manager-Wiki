# ICheckMovies Builders

You can find items using the lists on [icheckmovies.com](https://www.icheckmovies.com/) (ICheckMovies). 

No configuration is required for these builders.

| Name                                            | Attribute                   | Description                                                                                                         | Works with Movies | Works with Shows | Works with Playlists and Custom Sort |
|:------------------------------------------------|:----------------------------|:--------------------------------------------------------------------------------------------------------------------|:-----------------:|:----------------:|:------------------------------------:|
| [ICheckMovies List](#icheckmovies-list)         | `icheckmovies_list`         | Finds every movie in the ICheckMovies List                                                                          |      &#9989;      |     &#10060;     |               &#9989;                |
| [ICheckMovies List Details](#icheckmovies-list) | `icheckmovies_list_details` | Finds every movie in the ICheckMovies List and updates the collection with the description of the ICheckMovies list |      &#9989;      |     &#10060;     |               &#9989;                |

## ICheckMovies List

Finds every movie in the ICheckMovies List.

The expected input is a ICheckMovies List URL. Multiple values are supported as either a list or a comma-separated string.

The `sync_mode: sync` and `collection_order: custom` Details are recommended since the lists are continuously updated and in a specific order. 

```yaml
collections:
  Vulture’s 101 Best Movie Endings:
    icheckmovies_list: https://www.icheckmovies.com/lists/academy+award+-+best+picture
    collection_order: custom
    sync_mode: sync
```

* You can update the collection details with the ICheckMovies List's description by using `icheckmovies_list_details`.
* You can specify multiple collections in `icheckmovies_list_details` but it will only use the first one to update the collection summary.

```yaml
collections:
  Vulture’s 101 Best Movie Endings:
    icheckmovies_list_details: https://www.icheckmovies.com/lists/academy+award+-+best+picture
    collection_order: custom
    sync_mode: sync
```
