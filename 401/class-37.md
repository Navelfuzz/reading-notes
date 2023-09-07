# CF 401: Java // Reading Notes

## Class 37: Amazon S3 & Amplify

## Readings

[Introduction to Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html)

### Questions

1. What is Amazon S3?
2. List at least 3 features that it offers to its users.
3. What is an object key?

### Answers

1. Amazon S3 (Simple Storage Service):
* Amazon S3 is an object storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve data, including files, documents, images, videos, and backups, over the internet. S3 offers scalable and highly durable storage infrastructure, making it a fundamental building block for many cloud applications.
2. Features of Amazon S3:
* Scalability: Amazon S3 can store an unlimited amount of data, and it automatically scales to accommodate your storage needs. You can start with a small amount of data and expand as your requirements grow.
* Durability and Availability: S3 is designed for 99.999999999% (11 nines) durability, meaning your data is highly resilient to hardware failures and data loss. It also provides 99.99% availability, ensuring your data is accessible when needed.
* Data Security: S3 offers robust security features, including access control lists (ACLs), bucket policies, and identity and access management (IAM) integration. You can control who can access your data and how they can access it.
3. Object Key in Amazon S3:
* In Amazon S3, an object key is a unique identifier for an object (file or data) within a bucket. It serves as the object's name within the bucket and is used to retrieve and manage objects. The object key is essentially the file path or name of the object within the bucket's namespace.
* For example, if you have a bucket named "my-bucket" and you upload an image named "my-image.jpg" into that bucket, the object key for that image would be "my-image.jpg." Object keys are case-sensitive and can include special characters. Each object within a bucket must have a unique object key.
* Object keys play a crucial role in organizing and managing data within an S3 bucket, as they are used to reference and access objects when performing operations like uploads, downloads, deletions, and listing objects within a bucket.

[S3 with Amplify](https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/)

### Questions

1. Which dependencies are needed to install Amplify AWS S3 to your ndroid application?
2. What is needed in order to upload data to your bucket?
3. What method(s) initialize(s) the Amplify Auth and Storage categories?

### Answers

1. Dependencies for Amplify AWS S3:

dependencies {
    // Core Amplify Library
    implementation 'com.amplifyframework:core:1.0.0'

    // Amplify AWS Storage category
    implementation 'com.amplifyframework:aws-storage-s3:1.0.0'
    
    // Other dependencies, including Amplify Auth if needed
}

2. Uploading Data to Your Bucket:

To upload data to your Amazon S3 bucket using Amplify, you'll typically need to do the following:

* Initialize Amplify: Before using any Amplify category, you need to initialize Amplify. You can do this in your app's `Application` class or any appropriate entry point in your app:

```java 
// Initialize Amplify
Amplify.configure(getApplicationContext());
```

* Configure AWS Amplify: Configure the AWS Amplify settings, including your AWS account credentials and the region where your S3 bucket is located. You can do this in your `amplifyconfiguration.json` file:

```json
{
  "auth": {
    "plugins": {
      "awsCognitoAuthPlugin": {
        "UserAgent": "aws-amplify-cli/2.0",
        "Version": "1.0",
        "IdentityManager": {
          "Default": {}
        },
        "AppClient": {
          "WebDomain": "your-auth-web-domain",
          "AppClientId": "your-app-client-id",
          "SignInRedirectURI": "your-redirect-uri",
          "SignOutRedirectURI": "your-logout-uri",
          "SignInRedirectURISignUp": "your-signup-uri"
        },
        "CognitoUserPool": {
          "Default": {
            "PoolId": "your-pool-id",
            "AppClientId": "your-app-client-id",
            "Region": "your-region"
          }
        },
        "Auth": {
          "Default": {
            "authenticationFlowType": "USER_SRP_AUTH",
            "loginMechanisms": ["AMAZON", "EMAIL"]
          }
        }
      }
    }
  },
  "storage": {
    "plugins": {
      "awsS3StoragePlugin": {
        "bucket": "your-s3-bucket-name",
        "region": "your-region"
      }
    }
  }
}
```

* Upload Data: Use Amplify's Storage category to upload data to your S3 bucket. You can use methods like Amplify.Storage.uploadFile() to upload files or Amplify.Storage.put() to upload data.

```java
// Upload a file to S3 bucket
Amplify.Storage.uploadFile(
    "myFileKey", // Object key
    new File("/path/to/local/file"), // Local file to upload
    result -> {
        Log.i("Amplify", "Successfully uploaded file: " + result.getKey());
    },
    error -> {
        Log.e("Amplify", "Upload failed", error);
    }
);
```

3. Initialize Amplify Auth and Storage:

* To initialize Amplify Auth and Storage categories, you can use the Amplify.addPlugin() method in your app's initialization code after configuring Amplify. Here's an example:

```java
// Initialize Amplify
Amplify.configure(getApplicationContext());

// Add Auth plugin
Amplify.addPlugin(new AWSCognitoAuthPlugin());

// Add Storage plugin
Amplify.addPlugin(new AWSS3StoragePlugin());

// Initialize Auth and Storage
Amplify.Auth.initialize();
Amplify.Storage.initialize(getApplicationContext());
```

This code initializes both the Amplify Auth and Storage categories after configuring Amplify with your settings.

Make sure to replace placeholders like `your-auth-web-domain`, `your-app-client-id`, `your-pool-id`, `your-region`, `your-redirect-uri`, `your-logout-uri`, `your-signup-uri`, `your-s3-bucket-name`, and others with your actual AWS and authentication details.
