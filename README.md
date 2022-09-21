After adding:

implementation platform('com.google.cloud:libraries-bom:26.1.1')<br/>
implementation 'com.google.cloud:google-cloud-kms'

During Rebuilding Project I got an error message specifically:

Duplicate class com.google.api.Advice found in modules jetified-proto-google-common-protos-2.9.2 (com.google.api.grpc:proto-google-common-protos:2.9.2) and jetified-protolite-well-known-types-18.0.0-runtime (com.google.firebase:protolite-well-known-types:18.0.0)<br/>
...

You can simulate these errors if you try to build the project: Build > Make Project

I want to apply John Engelman's conflicting dependency shading plugin:<br/>
https://imperceptiblethoughts.com/shadow/

And shade com.google.api.grpc:proto-google-common-protos:2.9.2, but I can't do it.
