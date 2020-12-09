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
If there are, the API will return "OK". Else it will return an error message (depending on error)
Url : `http://<api_ip>:<api_port>/wallet/getbalance/<username>/<password>`

#### Checking balance
For checking balance, send a GET request to this url : `http://<api_ip>:<api_port>/wallet/getbalance/<username>/<password>`
Then the balance is returned as a text message.

#### Sending a transaction
For sending a transaction, send a GET request to this url : `http://<api_ip>:<api_port>/wallet/sendtx/<username>/<password>/<recipient>/<amount>`

#### Creating a duino-coin account
Send a GET request to this url `http://<api_ip>:<api_port>/wallet/sendtx/<desired_username>/<desired_password>/<email>`
*Email field is also required (but you can try a fake email hehe)*
