## hello-elasticsearch – Elasticsearch site plugin

A slightly modified Karel Minarik’s
[World's Smallest Application Hosted in Elasticsearch](https://gist.github.com/karmi/3381710/).

This is a small, self-contained HTML applications for Elasticsearch:

```
|-- css
|   |-- main.css
|   `-- normalize.css
|-- index.html
`-- README.md
```

Install this plugin with this command:

```sh
sudo /usr/share/elasticsearch/bin/plugin -install wbzyl/hello-elasticsearch
```

The files *index.html* and *README.md* are copied into
*/usr/share/elasticsearch/plugins/hello-elasticsearch/_site* folder.

After install the application will be available at
[http://localhost:9200/_plugin/hello-elasticsearch/index.html](http://localhost:9200/_plugin/hello-elasticsearch/index.html)

This application works with Elasticsearch version 0.90.6:

```json
{
  "nodes": {
    "LOqA0qc5QbOOWaWNd5Ou8A": {
      "http_address": "inet[/192.168.0.100:9200]",
      "version": "0.90.6",
      "hostname": "localhost.localdomain",
      "transport_address": "inet[/192.168.0.100:9300]",
      "name": "Heart Attack"
    }
  },
  "cluster_name": "wlodek",
  "ok": true
}
```
