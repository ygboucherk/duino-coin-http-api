# duino-coin-http-api
An HTTP api for duino-coin ! 

## duino-coin 
[Duino-Coin](https://github.com/revoxhere/duino-coin) is a cryptocurrency that was intended to be mineable with anything (yes, anything, including arduino boards).

## installing
First, you should install flask API module using pip :
`pip install flask`
And then run python script.

For enabling the faucet, you should set variable "enable_faucet" to True


## API documentation
All requests are made using GET, so you can try this API from your browser, without anything to change.

### Wallet
#### Checking login
Because of all other requests run without logging in, you may ask yourself the purpose of this function.
It's only for checking if credentials valid.
If there are, the API will return `OK`. Else it will return an error message (depending on error)
Url : 

`http://<api_ip>:<api_port>/wallet/getbalance/<username>/<password>`

#### Checking balance
For checking balance, send a GET request to this url : 


`http://<api_ip>:<api_port>/wallet/getbalance/<username>/<password>`


Then the balance is returned.

#### Sending a transaction
For sending a transaction, send a GET request to this url : 


`http://<api_ip>:<api_port>/wallet/sendtx/<username>/<password>/<recipient>/<amount>`


Then feedback (from DUCO server) is returned

#### Creating a duino-coin account
Send a GET request to this url 


`http://<api_ip>:<api_port>/wallet/sendtx/<desired_username>/<desired_password>/<email>`


*Email field is also required (but you still can try a fake email hehe)*

#### Changing password
Send a get request to this url :

`http://<api_ip>:<api_port>/wallet/changepasswd/<username>/<old_password>/<new_password>`


#### Getting DUCO email and ranking
For getting DUCO email username, send a GET request to this url : 


`http://<api_ip>:<api_port>/wallet/userstats/<username>/<password>`

####

Getting server address. For getting DUCO server address, send a GET request to this url : 

`http://<api_ip>:<api_port>/ducoserverip`

### Faucet
For claiming, send a GET a get request to 


`http//<api_ip>:api_port/faucet/<username>`


Please note that faucet should be enabled on the selected server
