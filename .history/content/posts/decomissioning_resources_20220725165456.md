---
title: "Decomissioning AWS services"
tags: [K7,K13, K20,K21,S17,S18]
---

![](../carbon.png)

data "aws_lambda_invocation" "json_request_12" {
  function_name = "migrate_lambda"
  provider      = aws.prod-burbank
  depends_on    = [aws_lambda_function.test_lambda]
  input         = jsonencode({"source"="tf-eu-west-2-terraform-burbank-ppb-test","destination"="dwp-ucfs-ppb-prod"})
}
