# CloudEvents-as-SSE
Simple demo of sending CloudEvents as Server Sent Events using Go.

From one terminal window run the command:
curl -v localhost:8008/events \
-X GET

From another terminal window POST a CloudEvent: 
curl -v localhost:8080/events \
-X POST \
-H "Ce-Id: 1234" \
-H "Ce-specversion: 0.3" \
-H "Ce-Type: cloudevents.sse.demo" \
-H "Ce-Source: cloudevents.sse.demo/CEsource" \
-H "Content-Type: application/json" \
-d '{"msg":"Hello World from the curl pod."}'

