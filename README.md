# Around-a-Geo-index-based-social-network
The big picture of this project:
![1556129800773](https://user-images.githubusercontent.com/40250261/56683477-7c60a180-6682-11e9-8460-75e318303aa9.jpg)
I write this project on Google Cloud Platform and edit code on GCE VM instance.

main.go:
handle post request and search request

GCE:
search: use ElasticSearch(GeoIndex). To use ES, we need to create post index in ES. We could also save post data to ES(NoSQL + Query Optimization), saveToES(use it when handle the post)
we could also read from ES for search, used in handlesearch

GCS(object storage):
save post image to GCS, used in handlerpost

BigTable: NoSQL + Cloud, persistent, offline analysis
saveToBigTable
![image](https://user-images.githubusercontent.com/40250261/56684813-5d174380-6685-11e9-92ec-cc0079937cb8.png)

BigQuery: Cloud version of SQL
code edited in Google Cloud terminal

Google Cloud ML:
just use the face sample to experience machine learning on GCP
ml.go

add token-based authentication
user.go
checkuser, adduser, handlelogin, handlesignup
Use JWT to Protect Post and Search Endpoints, need to verify token after logged in

use docker to pack up the whole project and publish it on dockerhub
GKE: Google Kubernetes Cluster
manage a production-grade cluster with high performance
