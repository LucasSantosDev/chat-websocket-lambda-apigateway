## Chat Websocket Real Time (Lambda | ApiGateway)

### Example

See this video!

<video width="100%" height="100%" controls>
  <source src="example.mp4" type="video/mp4">
</video>

### Config Lambda

Create a Lambda and set the code.

> Put the URL from `@connections URL` in action.js (remove https://)

```bash
URLWITHOUTHTTPS.com/STAGE/
```

> Attach policy to lambda policies (AmazonAPIGatewayInvokeFullAccess)

```bash
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["execute-api:Invoke", "execute-api:ManageConnections"],
      "Resource": "arn:aws:execute-api:*:*:*"
    }
  ]
}
```

---

### Config ApiGateway

<img src="./api-gateway-1.png" alt="step 1" />

<img src="./api-gateway-2.png" alt="step 2" />

<img src="./api-gateway-3.png" alt="step 3" />

<img src="./api-gateway-4.png" alt="step 4" />

<img src="./api-gateway-5.png" alt="step 5" />

<img src="./api-gateway-6.png" alt="step 6" />

---

### Config Frontend

> Put the URL from WSS in App.tsx (replace for WSS URL from ApiGateway)

```bash
wss://URLWSS.com/STAGE
```
