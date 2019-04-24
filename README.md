# Around-a-Geo-index-based-social-network
Here is the big picture of this project:
![1556129800773](https://user-images.githubusercontent.com/40250261/56683477-7c60a180-6682-11e9-8460-75e318303aa9.jpg)

## OAuth
I add token-based authentication for this project. user.go handles login and signup based on Elastic Search. main.go use JWT to protect post and search endpoints. When we do the requests, we need to add token to verify the identity.

## GKE
I use GKE to manage a production-grade cluster with high performance. For this part, I pack up the project in Docker and publish it to dockerhub.

## GCS
This part is an assistance for Elastic Search. I save images to GCS and it's used when handling post in main.go.

## GCE
This is the nerve center of the peoject. I search with Elastic Search based on GeoIndex(query optimization) and save post to Elastic Search.
I tried machine learning with ml.go. I didn't build my own library. I just use the face sample for an experience.

## Data analysis
BigTable and BigQuery are used for data analysis.
![image](https://user-images.githubusercontent.com/40250261/56684813-5d174380-6685-11e9-92ec-cc0079937cb8.png)
