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




### Not yet documented
            "languages", "countries", "contact-firstname", "contact-lastname", "contact-email",
            "contact-phone", "devices", "platform", "customs", "duration", "link", "info", "priority",
            "minutes", "contactVia", "contactViaDetails", "description", "expert-exclusion", "title", "venue",
            "billing-company", "billing-address", "billing-address2", "billing-zip", "billing-city", "billing-country",
            "billing-instructions", "billing-email", "location-company", "location-address",
            "location-zip", "location-city", "location-country", "location-instructions", "deadline",
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
