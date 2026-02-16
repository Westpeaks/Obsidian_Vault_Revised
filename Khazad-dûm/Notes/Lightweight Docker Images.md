2025-02-18 17:15

Tags: [[Khazad-dûm/Tags/Docker]] [[GitLab CI CD for DevOps Index]] [[CI CD]] 

- When running pipe in Gitlab, the Docker image must be downloaded before the first job can run. The bigger the image that must be downloaded, the longer it will take a job to run. 
- This is where lightweight images can provide a serious advantage. 

### Downloading a Lightweight Image

- Docker pulls and downloads images from its official repository by default. 
- These repos often provide lightweight versions. The following link provides further detail [Hubspot.Docker](https://hub.docker.com/). 
- For example, the official node image from Docker provides the following images. 
```
	node:<version>
```

```
	node:<version>-apline
```

```
	node:<version>-slim
```

- Each of these can be pulled into a pipeline for download and execution. The Alpine Linux and Slim version use much less data. 

### Alpine vs Slim

- The Alpine Linux distro is a popular small distribution of Linux (5MB) geared toward use cases such as CI/CD. It is a completely stripped down common Linux tools, such as bash, will need to be added in the Dockerfile.   
- The slim version provides a slim version of the original package as the name suggests. It will typically only contain the minimal packages necessary to run the desired image and in many cases the default image should just be used in its stead.    

## References

[Official Node Docker Image](https://hub.docker.com/_/node)



