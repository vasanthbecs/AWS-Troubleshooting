Amazon S3 allows you to set per-file permissions to grant read and/or write access. This is nice, but sometimes you just want to share your whole bucket with the world.Luckily, Amazon features bucket policies, which allow you to define permissions for an entire bucket. ~ This example will give read access to Everyone on all files in your bucket.
### Steps
1. Sign in to Amazon Web Services and go to your S3 Management Console.

2. Select the bucket from the left. At right, click the Properties button if it’s not already expanded.

3. Go to the Permissions tab and hit the Add Bucket Policy link. (If you’ve previously added a policy, the button will say Edit Bucket Policy instead).

![Image](D:\Vasanth\Docker\S3 policy)
