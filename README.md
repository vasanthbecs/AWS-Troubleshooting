Amazon S3 allows you to set per-file permissions to grant read and/or write access. This is nice, but sometimes you just want to share your whole bucket with the world.Luckily, Amazon features bucket policies, which allow you to define permissions for an entire bucket. ~ This example will give read access to Everyone on all files in your bucket.
### Steps
1. Sign in to Amazon Web Services and go to your S3 Management Console.

2. Select the bucket from the left. At right, click the Properties button if it’s not already expanded.

3. Go to the Permissions tab and hit the Add Bucket Policy link. (If you’ve previously added a policy, the button will say Edit Bucket Policy instead).

![s3 policy](https://cloud.githubusercontent.com/assets/24250130/26380090/7cc09042-3fea-11e7-8006-e5e0e4abd70b.png)
![s3 policy2](https://cloud.githubusercontent.com/assets/24250130/26380180/0d904d10-3feb-11e7-85f8-0e1405dc35ed.png)

```{
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
