---
title: "Decomissioning AWS services"
tags: [K7,K13, K20,K21,S17,S18]
---

![](../carbon.png)

```go
func invocation(function_name string, provider string, m map[string]string, n int) {
 f := hclwrite.NewEmptyFile()
 rootBody := f.Body()
 rootBody.AppendNewline()

 resourceBlock := rootBody.AppendNewBlock("data", []string{"aws_lambda_invocation", "json_request_" + strconv.Itoa(n)})
 resourceBody := resourceBlock.Body()

 resourceBody.SetAttributeValue("function_name", cty.StringVal(function_name))
 provider_tokens := hclwrite.Tokens{
  {
   Type:  hclsyntax.TokenIdent,
   Bytes: []byte(provider),
  },
 }
 resourceBody.SetAttributeRaw("provider", provider_tokens)

 depends_tokens := hclwrite.Tokens{
  {
   Type:  hclsyntax.TokenIdent,
   Bytes: []byte(`[aws_lambda_function.test_lambda]`),
  },
 }
 resourceBody.SetAttributeRaw("depends_on", depends_tokens)

 values := mapToString(m)
 tokens := hclwrite.Tokens{
  {
   Type:  hclsyntax.TokenIdent,
   Bytes: []byte(`jsonencode({` + values + `})`),
  },
 }

 resourceBody.SetAttributeRaw("input", tokens)
 fmt.Printf("%s", f.Bytes())
 fmt.Printf("\n")

}

```
