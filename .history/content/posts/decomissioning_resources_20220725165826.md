---
title: "Decomissioning AWS services"
tags: [K7,K13, K20,K21,S17,S18]
---

![](../carbon.png)

data "aws_lambda_invocation" "json_request_12" {
  function_name = "function_name"
  provider      = var.account
  depends_on    = [aws_lambda_function.test_lambda]
  input         = jsonencode({"source"="tf-eu-west-2-terraform-burbank-ppb-test","destination"="dwp-ucfs-ppb-prod"})
}
