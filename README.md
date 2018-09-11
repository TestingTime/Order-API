# Order-API

Documentation for the Prefill-API of our order form

## Url

Our orderform can be accessed in 3 languages: English, German & French

English: https://app.testingtime.com/en/order-testusers/{amount-of-users}/{method}<br/>
German: https://app.testingtime.com/de/testpersonen-bestellen/{amount-of-users}/{method}<br/>
French: https://app.testingtime.com/fr/commande-participants-aux-tests/{amount-of-users}/{method}

### Url-Parameters

| Parameter   	| Description   	| Type   	| Constraints   	| Other  	|
|---	|---	|---	|---	|---	|
| amount-of-users   	| How many users will be recruited   	| number   	| 3-300  	|   	|
| method  	| The method of the study that will be conducted  	| string  	| usertest<br/> workshop<br/> interview<br/> focusgroup<br/> survey<br/> diary  	|   	|

## Query 

Many fields on the order form can be prefilled. Here are all the supported parameters. They are all optional.

### Query-Parameters (GET)

| Parameter   	| Description   	| Type   	| Constraints   	| Other  	|
|---	|---	|---	|---	|---	|
| min-age   	| Minimal age of the ordered participants.   	| number   	| 18-85  	| Only works if you provide a max-age as well  	|
| max-age  	| Maximal age of the ordered participants.  	| number  	| 18-85  	| Only works if you provide a min-age as well. Must be at least 10 years more than the min-age.  	|
| gender  	| Gender mix if relevant.  	| string  	| female<br/>male<br/>mixed  	|   	|
| languages  	| Languages a test user needs to speak at least fluently  	| string  	| de<br/>fr<br/>en<br/>it<br/>nl  	| Comma separated if multiple. Max 2.  	|
| countries  	| Countries where the test users have to currently live at. 	| string  	| 2 digit ISO-Code - lowercase| Comma separated if multiple. Max 10.	|
| contact-firstname  	| Customer contacts (study conductor) first name 	| string  	| 	|
| contact-lastname  	| Customer contacts (study conductor) last name 	| string  	| 	|
| contact-email  	| Customer contacts (study conductor) email 	| string  	| 	|
| contact-phone  	| Customer contacts (study conductor) phone 	| string  	| 	|
| billing-company  	| Customer billing address - company name 	| string  	| 	|
| billing-address  	| Customer billing address - address line 1 	| string  	| 	|
| billing-address2  	| Customer billing address - address line 2 	| string  	| 	|
| billing-zip  	| Customer billing address - zip code 	| string  	| 	|
| billing-city  	| Customer billing address - city name 	| string  	| 	|
| billing-country  	| Customer billing address - country 	| string  	| 2 digit ISO-Code - lowercase	|
| billing-instructions  	| Customer billing reference number 	| string  	| 	|
| billing-email  	| Customer billing email address	| string  	| 	|
| location-company  	| Location of study - company name	| string  	| 	|
| location-address  	| Location of study - address line	| string  	| 	|
| location-zip  	| Location of study - zip code	| string  	| 	|
| location-city  	| Location of study - city name	| string  	| 	|
| location-company  	| Location of study - company name	| string  	| 	|
| location-country  	| Location of study - country	| string  	| 2 digit ISO-Code - lowercase	|
| location-instructions  	| Location of study - description how to find the location	| string  	| e.g. "ask at the reception for John Meyer"	|





### Not yet documented
            "devices", "platform", "customs", "duration", "link", "info", "priority",
            "minutes", "contactVia", "contactViaDetails", "description", "expert-exclusion", "title", "venue",
             "deadline",
            "priority", "link", "survey-by-redirect", "final-survey", "frequency", "slots", "inHomeModeOfTransport",
            "inviteRadius"
            
## Hashtag navigation

If you prefill all necessary information, you can choose the step of the order form that is shown at first.

| Value   	| Step-No   	| Description   |
|---	|---	|---	|
| #!/profile | 1 | Default - Select the users basic profile |
| #!/setup | 2 | Setup for your study<br/>Not available on method "survey" |
| #!/survey | 2 | Link and priority settings for survey<br/>Only available on method "survey" |
| #!/dates | 3 | Timing of your study<br/>Not available on methods "survey" & "diary" |
| #!/review | 3-4 | Review all your changes => **suggested if all necessary data is prefilled** |
| #!/payment | 4-5 | If you are sure all is already setup and you want to send the user to the payment step directly |
