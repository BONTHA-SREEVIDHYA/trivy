# trivy

Trivy is a powerful vulnerability scanner for containers and filesystems. This guide will walk you through the various ways to use Trivy for scanning folders and Docker images.   
Folder Scan   
To scan a folder or directory for vulnerabilities, use the following command:   
```sh
trivy fs path_to_scan
```
Example:   
```sh
trivy fs /path/to/scan
```
To save the scan result in HTML format, use the --format and -o options:   
```sh
trivy fs --format html -o result.html path_to_scan
```
Example:
```sh
trivy fs --format html -o result.html /path/to/scan
```
You can also specify the types of security checks to perform using the --security checks option:    
```sh
trivy fs --format html -o result.html --security-checks vuln,config
```
Folder_name_OR_Path   
Docker Image Scan : To scan a Docker image for vulnerabilities, use the following command:   
```sh
trivy image image_name
```
Example:   
```sh
trivy image my_image:latest
```
To save the scan result in HTML format, use the -f and -o options:   
```sh
trivy image -f html -o results.html image_name
```
Example:   
```sh
trivy image -f html -o results.html my_image:latest
```
You can specify the severity levels of vulnerabilities to include in the report using the --severity option:   
```sh
trivy image -f html -o results.htm --severity HIGH,CRITICAL image_name
```
Example: 
trivy image -f html -o results.html --severity HIGH,CRITICAL 
my_image:latest
