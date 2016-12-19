# gRPCPythonHelloWorld

This is a simple Hello World example for gRPC in python.
The examples are from [the grpc github repository](https://github.com/grpc/grpc/tree/master/examples/python).

# Usage

Enter the IP of your server in the `greeter_client.py` file in the `run` method.
It should look like this:

```
def run():
  channel = grpc.insecure_channel('yourIpHere:50505')
  stub = helloworld_pb2.GreeterStub(channel)
  response = stub.SayHello(helloworld_pb2.HelloRequest(name='you'))
  print("Greeter client received: " + response.message)
```