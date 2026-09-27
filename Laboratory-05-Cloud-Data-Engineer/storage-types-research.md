
## Types of Cloud Storage

| Storage Type       | Simple Description                                                                                                | Main Use                                                                                | Cloud Provider Example |
| ------------------ | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ---------------------- |
| **Block Storage**  | Divides data into small blocks and stores them like a hard drive.                                                 | Good for databases, virtual machines, and operating systems that need fast performance. | AWS EBS                |
| **File Storage**   | Stores data as files inside folders and directories. Many users or computers can access the files.                | Good for shared files, documents, and folders.                                          | AWS EFS                |
| **Object Storage** | Stores data as individual objects, such as images, videos, and files. Each object has its own ID and information. | Good for storing large amounts of photos, videos, backups, and other files.             | AWS S3                 |

## Why Use Object Storage for User-Uploaded Images?

**Object Storage is a good choice for storing users' uploaded images** because it can handle a very large number of files. You don't need to worry about running out of space because it can easily grow as more images are added.

Each image can have its own information and unique link, making it easy for websites and apps to access. It also helps keep images safe by storing copies in different locations. This means the images can still be available even if one server has a problem.

