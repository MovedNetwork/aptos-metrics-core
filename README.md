## Patch to use the prometheus protobuf feature

Currently, the Aptos metrics crate uses the plain `Vec` to set labels, however Sui uses the `protobuf::RepeatedField` instead.
The easiest way to make them both happy is to make them both use the recommended `protobuf` feature.