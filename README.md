# build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito

* based on [Serverless Web Application Workshop](https://github.com/aws-samples/aws-serverless-workshops/blob/master/WebApplication/README.md) and [Build a Serverless Web Application](https://aws.amazon.com/getting-started/projects/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/)
* good example showing cognito registration, verification, and signin with S3 static website
    * see [`src/1_StaticWebHosting/website/js/cognito-auth.js`](src/1_StaticWebHosting/website/js/cognito-auth.js) for details register, verify, signin
        * `WildRydes.authToken` method
        ![](https://www.evernote.com/l/AAHZxEdxOZtIdLlWyw2Qkz5qyv4K_UGkRKAB/image.png)
        * authorized API Gateway request
        ![](https://www.evernote.com/l/AAElbTXGfHhK5ZyctvX55_Za4AUKChN7uIEB/image.png)

    > NOTE: web in browser cognito SDK stores identity (JWT token) information in `localStorage`.  This is what allows maintaining session credentials across page reloads.