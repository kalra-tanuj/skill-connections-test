# skill-connections-test

This is a gamma-skill created on  https://developer-gamma.amazon.com/alexa/console/ask.

Steps to check the working of skill-connections

1. Open the test tab of developer-gamma.amazon.com and say/type open requester gamma
2. now say/type skill connections
3. Upon saying skill connections intent, TestIntentHandler will be called, which will start a skill-connection. 
4. Since 'onCompletion': 'RESUME_SESSION' is passed in .addDirective of TestIntentHandler, after the execution of TestIntentHandler is completed, control will be sent to this function - SessionResumedRequestHandler.
5. Check for the JSON Input 2/2 in the right side after type/calling skill connections, you will see a json with response 200 in the end.

"request": {
		"type": "SessionResumedRequest",
		"requestId": "amzn1.echo-api.request.c8d26319-a780-4d28-855f-b74866373e6f",
		"timestamp": "2022-08-25T13:22:49Z",
		"locale": "en-US",
		"cause": {
			"type": "ConnectionCompleted",
			"token": "...",
			"status": {
				"code": "200",
				"message": "OK"
			}
		}
	}

