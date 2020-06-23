# AWSSQS

AWS SQS Interface for Julia

[![Build Status](https://travis-ci.org/JuliaCloud/AWSSQS.jl.svg)](https://travis-ci.org/JuliaCloud/AWSSQS.jl)
[![ColPrac: Contributor's Guide on Collaborative Practices for Community Packages](https://img.shields.io/badge/ColPrac-Contributor's%20Guide-blueviolet)](https://github.com/SciML/ColPrac)


[Documentation](https://juliacloud.github.io/AWSCore.jl/build/AWSSQS.html)

```julia
using AWSSQS

aws = AWSCore.aws_config()

q = sqs_get_queue(aws, "my-queue")

sqs_send_message(q, "Hello!")

m = sqs_receive_message(q)
println(m[:message])
sqs_delete_message(q, m)
```
