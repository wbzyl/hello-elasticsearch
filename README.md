## hello-elasticsearch — elasticsearch site plugin

[World's Smallest Application Hosted in Elasticsearch](https://gist.github.com/karmi/3381710/) by K. Minarik.

This makes it easy to create small, self-contained HTML applications
for elasticsearch, just like this one:

```
.
|-- index.html
`-- README.md

```

Install:

```sh
sudo /usr/share/elasticsearch/bin/plugin -install wbzyl/hello-elasticsearch
```

Po instalacji pliki *index.html* oraz *README.md* znajdziemy
w katalogu */usr/share/elasticsearch/plugins/hello-elasticsearch/_site*


After install the application will be available at
[http://localhost:9200/_plugin/hello-elasticsearch/index.html](http://localhost:9200/_plugin/hello-elasticsearch/index.html)


### *index.html*


```json
{
  "nodes": {
    "LOqA0qc5QbOOWaWNd5Ou8A": {
      "http_address": "inet[/192.168.0.100:9200]",
      "version": "0.90.6",
      "hostname": "localhost.localdomain",
      "transport_address": "inet[/192.168.0.100:9300]",
      "name": "Page, Karen"
    }
  },
  "cluster_name": "wlodek",
  "ok": true
}
```


### CORS (does not work with IE?)

JavaScript

```html
console.log('is CORS supported?', $.support.cors);  # dopisać

$.getJSON('http://localhost:9200/_cluster/nodes/_local', function(data) { … }
```

ze strony *index.html* zadziała jeśli uruchomimy server WWW,
który zaserwuje tę stronę, na przykład serwer *serve* z pakietu Node.js:

```sh
npm install -g serve
```


### bulk import

TODO: import imieniny
