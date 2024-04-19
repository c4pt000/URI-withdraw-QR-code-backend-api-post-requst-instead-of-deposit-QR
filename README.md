# pseudocode idea right now no working basic code

normally everyone everywhere everyday uses QR codes to deposit from their mobile to a website address

example

![s1](https://raw.githubusercontent.com/c4pt000/URI-withdraw-QR-code-backend-api-post-requst-instead-of-deposit-QR/main/deposit-select.png)

but what if you select to withdraw instead of deposit and you wanted an easy way to do it by "selecting your withdrawl address on your phone application and then a button to scan withdraw address?"


![s1](https://raw.githubusercontent.com/c4pt000/URI-withdraw-QR-code-backend-api-post-requst-instead-of-deposit-QR/main/qr-withdraw.png)


![s1](https://raw.githubusercontent.com/c4pt000/URI-withdraw-QR-code-backend-api-post-requst-instead-of-deposit-QR/main/withdraw-select.png)

[1] selecting your withdraw address on your mobile device and clicking a button for "scan withdrawal QR code" 

would read the withdrawal QR code on the website which would be an encoded URI string for the server's api listening for input using that string linked to your username


URI-encoded string example.... "user999@api.xeggex.com?t=<dateandtimeinunixepoch>-<randomized-64-length-hash-here>"

once you scan the withdraw code on your mobile after selecting your address that you want to withdraw to which would arrive on your phone.....


the mobile app would input the withdraw QR code it would read the username@host.com in the string and the datetimestamp in the random string and it would read the randomized-64-length-hash-string

and the mobile app would then take the withdraw address you selected and do a POST request to push the withdraw address you selected from your phone to the server's remote api that is listening for incoming post requests from different user's address (when the user actually requests it)


once the remote server recieves the post request which is listening for remote input (almost similar to post tx/rawtx from bitcoin rpc but for a select URI-sring-with-address-and-username)

[2] the website javascript or php script where the user wants the withdraw address inputed instead of manually inputing the withdraw address will automatically be inserted and show up then the user can click withdraw to proceed withdrawing funds

would be inserted into the page from the api's backend



then once the withdraw address has 1 confirm or a pre-confirm for a tx from the user actually withdrawing funds or some action

then the api marks the string as received withdraw address

and generates a new withdraw QR code address with a different timestamp every single time the user wants to scan a new withdraw address in


