### Common commands
___
**Sort files by date and show the most recent 5 files**
```
ls -lt | head -5
```
### SSH commands
___
**Upload file by SSH to remote host**
```
scp -i <key_file> <archive_to_upload> <user>@<ip>:<target_folder>
example: scp -i id_rsa uploader-0.5.4.zip root@165.22.250.243:/home/nazarb
```
**Download file from remote host by SSH**
```
scp -i <key_file> <user>@<ip>:<remote_path> <local_folder>
example: scp -i id_rsa root@165.22.250.243:/tmp/uploader-0.5.4.zip .
```

### Working with different archive types
_____
**Create a Zip archive from folder and exclude files**
```
example: zip -r <archive_name>.zip <folder_to_be_archived> -x *.git* -x *node_modules* -x .env
```
**Unzip archive to a specific folder**
```
example: unzip az-blob-plugin-1.6.2.zip -d /mnt/c/tools/kafka-connect-plugins
```
**Untar gz archive to a specific folder**
```
tar -xzvf <archive_name> -C <destination_name>
example: tar -xzvf kafka_2.13-2.8.0.tgz -C /tmp/test-out
```
**Create a tar archive**
```
tar -czvf <archive_name> <folder_to_be_archived>
example: tar -czvf test-out.tgz kafka_2.13-2.8.0/
```

**Setup port forwarding**
ssh -i id_rsa  -L 9001:<remote_host>:9001 -N <username>@<remote_host>



