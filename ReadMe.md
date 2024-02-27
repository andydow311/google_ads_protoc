If you wish to create the Golang files from the upload_click_conversions.proto file in this repo then:

1. Ensure that proto-gen-go is installed and working on your machine:  https://grpc.io/docs/languages/go/quickstart/
2. Create a folder <project_name> and move into using command: cd <project_name>
3. Once in the project, at directory level, clone in the googleapis library using command: git clone https://github.com/googleapis/googleapis/tree/master/google
4. Once library is cloned, make a directory for your proto file using command mkdir <proto_folder_name>. Copy and paste the upload_click_conversions.prot from this repo to the new directory.

After stage 4 the project directory should look like this:

```
<project_name>
|
------ google
|        |
|        ------ api
|              |
|              ------ annotations.proto
|              |
|               ------ http.proto
|
------ <proto_folder_name>
               |
               |
                ------  upload_click_conversions.proto
```

5. Opening a terminal window at the project level above <project_name>, running the following command will generate the Go code within the <proto_folder_name> folder:


protoc -I ./<project_name> \                                            
--go_out ./<project_name>/<proto_folder_name> --go_opt paths=source_relative \
 --go-grpc_out ./<project_name>/<proto_folder_name> --go-grpc_opt paths=source_relative \
./<project_name>/<proto_folder_name>/upload_click_conversions.proto


Further details can be found here: https://grpc-ecosystem.github.io/grpc-gateway/docs/tutorials/simple_hello_world/