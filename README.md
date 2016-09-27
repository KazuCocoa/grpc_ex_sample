# GrpcExSample

Example of https://github.com/bitwalker/exprotobuf to understand protocol buffer.

# related links

- Protocol Buffer
    - https://github.com/google/protobuf
- A Google Protobuf implementation for Erlang
    - https://github.com/tomas-abrahamsson/gpb

# Example

```
$ iex -S mix

$ GrpcExSample.defs
[{{:service, GrpcExSample.Greeter},
  [{:rpc, :SayHello, :HelloRequest, :HelloReply, false, false, []}]},
 {{:msg, GrpcExSample.HelloRequest},
  [%Protobuf.Field{fnum: 1, name: :name, occurrence: :optional, opts: [],
    rnum: 2, type: :string}]},
 {{:msg, GrpcExSample.HelloReply},
  [%Protobuf.Field{fnum: 1, name: :message, occurrence: :optional, opts: [],
    rnum: 2, type: :string}]},
 {{:msg, GrpcExSample.Msg.SubMsg},
  [%Protobuf.Field{fnum: 1, name: :value, occurrence: :required, opts: [],
    rnum: 2, type: :uint32}]},
 {{:enum, GrpcExSample.Msg.Version}, [V1: 1, V2: 2]},
 {{:msg, GrpcExSample.Msg},
  [%Protobuf.Field{fnum: 2, name: :version, occurrence: :required, opts: [],
    rnum: 2, type: {:enum, GrpcExSample.Msg.Version}},
   %Protobuf.Field{fnum: 1, name: :sub, occurrence: :optional, opts: [],
    rnum: 3, type: {:msg, GrpcExSample.Msg.SubMsg}}]}]
```
