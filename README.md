# Downsize that image !

The docker-compose.yaml at the root defines a receiver proxy server which has an only purpose: decompress gzip-ed incoming requests and forward it to the backend service.

You can check the service is correctly doing it's job with the following command:
`echo "{'content':'hey'}" | gzip | curl -X POST --header "Content-Encoding: gzip" --data-binary @- http://localhost:8081`

The current docker image is 200MB big!

**Your task is to downsize the image size (while still keeping it functional).**

Also, keep everything inline if possible so the solution can be run and shared easily.
