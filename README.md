# Public Readable Amazon S3 Bucket Policy
Amazon S3 allows you to set per-file permissions to grant read and/or write access. This is nice, but sometimes you just want to share your whole bucket with the world.Luckily, Amazon features bucket policies, which allow you to define permissions for an entire bucket. ~ This example will give read access to Everyone on all files in your bucket.
### Steps
1. Sign in to Amazon Web Services and go to your S3 Management Console.

2. Select the bucket from the left. At right, click the Properties button if it’s not already expanded.

3. Go to the Permissions tab and hit the Add Bucket Policy link. (If you’ve previously added a policy, the button will say Edit Bucket Policy instead).

![s3 policy](https://cloud.githubusercontent.com/assets/24250130/26380090/7cc09042-3fea-11e7-8006-e5e0e4abd70b.png)
![s3 policy2](https://cloud.githubusercontent.com/assets/24250130/26380180/0d904d10-3feb-11e7-85f8-0e1405dc35ed.png)
### S3 readonly policy format
```
{
	"Version":"2008-10-17",
	"Statement":[{
	"Sid":"AllowPublicRead",
		"Effect":"Allow",
		"Principal": {
			"AWS": "*"
			},
		"Action":["s3:GetObject"],
		"Resource":["arn:aws:s3:::bucket/*"
		]
	}
	]
    } 
```
### Getting the URL for an Individual Object
There are a number of ways to share the contents of the bucket, from an individual URL for an individual object through making the bucket available to host a static website on a custom domain.
If you’re looking to quickly share the URL of a specific object, here’s one way to find the link:
```
1. Sign into the AWS Management Console and go to your S3 dashboard.
2. Navigate to the specific bucket and object.
3. Click on the Properties button at top right.
4. Copy the URL from the Link info at top right, which should look 
```
![](https://cdn.havecamerawilltravel.com/photographer/files/2013/03/Amazon-S3-link-to-shared-object-678x295.jpg)
