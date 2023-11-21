# aws-rekognition-test

Worked on some AWS services during an internship. Used a Lambda function to trigger everytime an image (PNG/JPG is supported) to a particular S3 bucket. Initially the files were hardcoded to test whether the Rekognition, S3 & Lambda worked. Now automated to detect any file & outputs the result to another bucket in JSON format for each face. (Only tried out the Detect Faces option so far.) Mostly many image & file uploads to S3 & detection capabilities by Rekognition are covered under the free trial.

The result JSON file will give attributes of the face like Wearing Glasses or Beard and their Emotions and many more features. It also gives the position of the face detected.

Basics made with the help of a video by Be a Better Dev on [Using Rekognition for Facial Analysis](https://www.youtube.com/watch?v=3PGPfs-ARdo). (The region for the Lambda function & S3 Bucket should be same or it cannot be accessed by the Lambda function. Spent some time on this.) Made the result S3 file dynamic from searching the web across multiple articles & Stack Overflow links but they were too complex for me. Finally got a simple solution from Be a Better Dev on [S3 & Lambda Triggers](https://www.youtube.com/watch?v=OJrxbr9ebDE). Don't remember where I got the upload to S3 result. But its the basic Offical Boto3 Docomentation on S3 uploads.

Spaces in file name cause errors in triggering the Lambda function. Do not know if any other special characters affect it.
