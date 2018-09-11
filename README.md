# Order-API

Documentation for the Prefill-API of our order form

## Url

Our orderform can be accessed in 3 languages: English, German & French

English: https://app.testingtime.com/en/order-testusers/{amount-of-users}/{method}<br/>
German: https://app.testingtime.com/de/testpersonen-bestellen/{amount-of-users}/{method}<br/>
French: https://app.testingtime.com/fr/commande-participants-aux-tests/{amount-of-users}/{method}

### Url-Parameters:

| Parameter   	| Description   	| Type   	| Constraints   	| Other  	|
|---	|---	|---	|---	|---	|
| amount-of-users   	| How many users will be recruited   	| number   	| 3-300  	|   	|
| method  	| The method of the study that will be conducted  	| string  	| usertest<br/> workshop<br/> interview<br/> focusgroup<br/> survey<br/> diary  	|   	|
