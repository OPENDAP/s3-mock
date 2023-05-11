# s3-mock

## How to use
A service to emulate S3 errant behavior

To start the service 'python3 main.py'

To emulate the S3 '500 message' behavior, send it http://localhost:8000/500/N/name.
For example, to emulate a 500 error on the request for three tries, send it 
http://localhost:8000/500/3/name and the service will return 3 HTTP 500 consecutive
errors before returning a 200 response. The 200 response will contain 183 characters.

Once started, the service can handle parallel requests but you need to use different
_name_ parts of the _path_ passed to the service.

To stop the server, send it http://localhost:8080/exit.

## Where to find
github.com/OPENDAP/s3-mock
