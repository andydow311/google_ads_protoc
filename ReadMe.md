
Protocol command (change directory (cd) into the file continaing the google_dds_protoc file ):

protoc -I ./google_dds_protoc \                                            
--go_out ./google_dds_protoc/uploadclicks/pb --go_opt paths=source_relative \
 --go-grpc_out ./google_dds_protoc/uploadclicks/pb --go-grpc_opt paths=source_relative \
./google_dds_protoc/uploadclicks/upload_click_conversions.proto