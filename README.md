# of-demo





## Create Group
```
curl -X 'PUT' \
  'https://databus.dbpedia.org/m1ci/openflaas_de' \
  -H 'accept: application/json' \
  -H 'X-API-KEY: YOUR_KEY' \
  -H 'Content-Type: application/ld+json' \
  -d '{
  "@context": "https://downloads.dbpedia.org/databus/context.jsonld",
  "@graph": {
    "@id": "https://databus.dbpedia.org/m1ci/openflaas_de",
    "@type": "Group",
    "title": "openflaas_demo group",
    "description": "Test group for OpenFLaaS."
  }
}'
```


## Create Artifact
```
curl -X 'PUT' \
  'https://databus.dbpedia.org/m1ci/openflaas_de/reviews' \
  -H 'accept: application/json' \
  -H 'X-API-KEY: YOUR_KEY' \
  -H 'Content-Type: application/ld+json' \
  -d '{
  "@context": "https://downloads.dbpedia.org/databus/context.jsonld",
  "@graph": {
    "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews",
    "@type": "Artifact",
    "title": "reviews Data",
    "description": "reviews description."
  }
}'
```
## Publish a files under an artifact version
```
curl -X 'PUT' \
  'https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26' \
  -H 'accept: application/json' \
  -H 'X-API-KEY: YOUR_KEY' \
  -H 'Content-Type: application/ld+json' \
  -d '{
  "@context": "https://downloads.dbpedia.org/databus/context.jsonld",
  "@graph": {
    "@type": [
      "Version",
      "Dataset"
    ],
    "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26",
    "hasVersion": "2025-03-26",
    "title": "MTL Dataset",
    "description": "Data for testing purposes.",
    "license": "http://creativecommons.org/licenses/by/4.0/",
    "distribution": [
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#MR.task.train",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "MR",
        "dcv:data_type": "train",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/MR.task.train"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#MR.task.test",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "MR",
        "dcv:data_type": "test",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/MR.task.test"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#MR.task.unlabel",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "MR",
        "dcv:data_type": "unlabel",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/MR.task.unlabel"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#apparel.task.unlabel",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "apparel",
        "dcv:data_type": "unlabel",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/apparel.task.unlabel"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#apparel.task.test",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "apparel",
        "dcv:data_type": "test",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/apparel.task.test"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#apparel.task.train",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "apparel",
        "dcv:data_type": "train",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/apparel.task.train"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#baby.task.unlabel",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "baby",
        "dcv:data_type": "unlabel",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/baby.task.unlabel"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#baby.task.test",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "baby",
        "dcv:data_type": "test",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/baby.task.test"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#baby.task.train",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "baby",
        "dcv:data_type": "train",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/baby.task.train"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#books.task.unlabel",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "books",
        "dcv:data_type": "unlabel",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/books.task.unlabel"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#books.task.test",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "books",
        "dcv:data_type": "test",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/books.task.test"
      },
      {
        "@id": "https://databus.dbpedia.org/m1ci/openflaas_de/reviews/2025-03-26#books.task.train",
        "@type": "Part",
        "formatExtension": "none",
        "compression": "none",
        "dcv:category": "books",
        "dcv:data_type": "train",
        "downloadURL": "https://github.com/m1ci/of-demo/raw/refs/heads/main/data/mtl-dataset/books.task.train"
      }
    ],
    "rdf:Property": {
      "@id": "https://dataid.dbpedia.org/databus-cv#category",
      "rdfs:subPropertyOf": "databus:contentVariant"
    },
    "rdf:Property": {
      "@id": "https://dataid.dbpedia.org/databus-cv#data_type",
      "rdfs:subPropertyOf": "databus:contentVariant"
    }
  }
}'
```

