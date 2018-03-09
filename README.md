# FTPApi
Create Object Instance
```cs
var ftpClient = new ftp(@"ftp://10.10.10.10/", "user", "password");
```
Upload a File
```cs
ftpClient.upload("etc/test.txt", @"C:\Users\metastruct\Desktop\test.txt");
```
Download a File
```cs
ftpClient.download("etc/test.txt", @"C:\Users\metastruct\Desktop\test.txt");
```
Delete a File
```cs
ftpClient.delete("etc/test.txt");
```
Rename a File
```cs
ftpClient.rename("etc/test.txt", "test2.txt");
```
Create a New Directory
```cs
ftpClient.createDirectory("etc/test");
```
Get the Date/Time a File was Created
```cs
string fileDateTime = ftpClient.getFileCreatedDateTime("etc/test.txt");
Console.WriteLine(fileDateTime);
```
Get the Size of a File
```cs
string fileSize = ftpClient.getFileSize("etc/test.txt");
Console.WriteLine(fileSize);
```
Get Contents of a Directory (Names Only)
```cs
string[] simpleDirectoryListing = ftpClient.directoryListDetailed("/etc");
for (int i = 0; i < simpleDirectoryListing.Count(); i++) { 
    Console.WriteLine(simpleDirectoryListing[i]); 
}
```
Get Contents of a Directory with Detailed File/Directory Info
```cs
string[] detailDirectoryListing = ftpClient.directoryListDetailed("/etc");
for (int i = 0; i < detailDirectoryListing.Count(); i++) { 
    Console.WriteLine(detailDirectoryListing[i]); 
}
```
