<!-- ![Logo](https://github.com/phanisaimunipalli/aws-insearch/blob/master/images/insearch_logo.png?raw=true) -->

![AWS InSearch Logo](/images/insearch_logo.png)

# AWS InSearch - `Now Search Less`

Did you ever thought of knowing products that you have seen in an Instagram Picture? or Causual browsing on Internet? Let me guess...you might have taken several text searches to find the closest match you saw in the image you saved.

Then Welcome to **InSearch**, it can make your search eaiser and less by just one upload, you will be able to find what is/are exactly in the image. This is powered by Serverless Framework, AWS Lambda and AWS Rekognition Cloud Services.

## Vision

The vision of AWS InSearch is to allow people to pause their Favorite TV Show or a Movie and tap the bed lamp on screen to get it's Amazon link. This is is a prototype of allowing to upload image to an S3 Bucket to identify objects in that scene.

## Tech Stack

NodeJS, [Serverless Framework ](https://github.com/serverless/), AWS Lambda, S3, IAM

## Deploy

Clone the project

```bash
  git clone https://github.com/phanisaimunipalli/aws-insearch.git
```

Go to the project directory

```bash
  cd aws-insearch
```

Install Serverless Framework

```bash
  npm i serverless
```

Install dependencies

```bash
  npm install
```

Configuration

`1. Create your AWS S3 bucket & IAM user.`

`2. Configure Access Keys using aws-cli`

`3. Update your handler.js file for any custom changes`

Run the serverless

```bash
  serverless deploy
```

Invoke using local post.json

```bash
  serverless invoke local -f imageAnalysis -p post.json
```

Invoke using CURL

```bash
  curl -X POST -H 'Content-Type:application/json' -d '{"bucket":"insearch-gallery","imageName":"cat.jpeg"}' https://8riwh3ld2g.execute-api.us-west-1.amazonaws.com/dev/analysis
```

## InSearch API

https://8riwh3ld2g.execute-api.us-west-1.amazonaws.com/dev/analysis

## Screenshots

**Sample Scene/Image**

![Sample Scene-insearch](https://github.com/phanisaimunipalli/aws-insearch/blob/master/images/table.jpeg?raw=true)

**API Request & Response**

![API Request Response](/images/aws-insearch-reqres.png?raw=true)

**IS-AWS S3 Bucket**

![IS-AWS S3](/images/aws-insearch-s3.png?raw=true)

**IS-AWS Lambda Function**

![IS-AWS Lambda](/images/aws-insearch-lambda.png?raw=true)

## Authors

- [Phani Sai Ram Munipalli](https://www.github.com/phanisaimunipalli)
