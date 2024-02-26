
Please follow instructions here to ensure that proto-gen-go is installed and working on your local host:  https://grpc.io/docs/languages/go/quickstart/


Protocol command (change directory (cd) into the file continaing the google_dds_protoc file ):

protoc -I ./google_ads_protoc \                                            
--go_out ./google_ads_protoc/uploadclicks/pb --go_opt paths=source_relative \
 --go-grpc_out ./google_ads_protoc/uploadclicks/pb --go-grpc_opt paths=source_relative \
./google_ads_protoc/uploadclicks/upload_click_conversions.proto