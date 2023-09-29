# Network requests: curl

- <https://medium.com/@dwyer.donovan/sending-http-requests-from-your-command-line-5ef6eecffb0a>
- <https://curl.se/docs/manpage.html>

## GET

```bash
# get only head of a request
curl --head GET '$URL'

# download files from the internet
curl -o mydownloadedfile.zip https://example.com/file.zip

# to upload a file, use the "-F" option
curl -F "file=@myupload.txt" https://example.com/upload

# by default, "curl" follows HTTP redirects, to disable automatic redirection and display the final URL and response, you can use the "-L" option
curl -L https://example.com/redirecting-url

# to access a resource that requires authentication, you can use the "-u" option to provide a username and password
curl -u username:password https://example.com/protected-resource

# to make HTTP POST requests to web services or APIs you can send data using the "-d" option
curl -d "key1=value1&key2=value2" -X POST https://example.com/api/endpoint

# to set custom request headers using the "-H" option
curl -H "Authorization: Bearer mytoken" https://example.com/api/resource

# to test if a server is reachable and responding
curl -I https://example.com

# get request and output the result to a file
curl --location --request GET '$URL' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer $USER_TOKEN' \
--output '$FILE_LOG.json'

curl --location --request GET 'http://localhost:8080/v1/api/gapi/search?source=enobot&name=pnl&ts_start=2023-09-09T00:00&ts_end=2023-09-09T23:59&time=local' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer xxxxxxx' \
--output '/Users/spetushkou/Projects/curl/doc/get_gapi_enobot_pnl.json'
```
