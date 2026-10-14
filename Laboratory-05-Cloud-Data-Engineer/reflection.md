
# Mission 5 Reflection – The Cloud Data Engineer

This laboratory activity helped me understand the importance of cloud storage and how it is used in real-world applications. I learned about Block Storage, File Storage, and Object Storage. Each type has its own purpose, depending on how data needs to be stored and accessed.

Object Storage is better suited for storing millions of photos because it is designed to handle large amounts of unstructured data. Unlike a traditional block storage hard drive, it stores data as objects with metadata and unique identifiers. This makes it a practical choice for a photo-sharing application because the images can be organized inside a bucket and accessed when needed.

Using Docker made it easier to deploy the MinIO storage server because I could run the service inside a container using a single command. I did not need to manually install and configure every component separately. I also learned how port mapping allows me to access the MinIO Web Console through a browser and how environment variables can be used to configure login credentials.

A bucket in cloud storage is a container used to organize objects, such as images, videos, and documents. In this activity, I created a bucket named `client-photos` and uploaded a sample file to test the storage service.

Large enterprise companies can reduce the risk of data loss by using data replication, backups, and redundant storage systems across multiple servers or locations. These methods help protect information if a physical server crashes, although proper monitoring and recovery planning are also important.

My confidence in navigating the Linux command line is gradually improving. At first, commands and Docker options seemed unfamiliar, but following the steps helped me understand their purposes. I also learned the importance of checking whether a container is running and reviewing its logs when problems occur. Overall, this activity improved my understanding of object storage, Docker, and cloud infrastructure. It also helped me practice documenting technical work using Markdown and GitHub.
