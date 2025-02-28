# Plex Attributes

Configuring [Plex](https://www.plex.tv/) is required in order to connect to your libraries. 

A `plex` mapping can be either in the root of the config file as global mapping for all libraries or you can specify the `plex` mapping individually per library. 

Below is a `plex` mapping example and the full set of attributes:
```yaml
plex:
  url: http://192.168.1.12:32400
  token: ####################
  timeout: 60
  clean_bundles: true
  empty_trash: true
  optimize: false
```

| Name                 | Attribute       | Allowed Values                                                         | Default | Required |
|:---------------------|:----------------|:-----------------------------------------------------------------------|:-------:|:--------:|
| Server URL           | `url`           | Plex Server URL<br><strong>Example:</strong> http://192.168.1.12:32400 |   N/A   | &#9989;  |
| Authentication Token | `token`         | Plex Server Authentication Token                                       |   N/A   | &#9989;  |
| Plex Timeout         | `timeout`       | Plex Server Timeout                                                    |   60    | &#10060; |
| Clean Bundles        | `clean_bundles` | Runs Clean Bundles on the Server after all Metadata Files are run      |  false  | &#10060; |
| Empty Trash          | `empty_trash`   | Runs Empty Trash on the Server after all Metadata Files are run        |  false  | &#10060; |
| Optimize             | `optimize`      | Runs Optimize on the Server after all Metadata Files are run           |  false  | &#10060; |

* This script can be run on a remote Plex server, but be sure that the `url` provided is publicly addressable and it's recommended to use `HTTPS`.

* If you need help finding your Plex authentication token, please see Plex's [support article](https://support.plex.tv/articles/204059436-finding-an-authentication-token-x-plex-token/).
