# bitcoin-balance-api-php

Easy-to-use API for retrieving the balance of a Bitcoin wallet with https://bitcoin-balance-api.com/

Swagger: https://api-testnet.bitcoin-balance-api.com/docs/

## Get Balance

```
#!/usr/bin/env php
<?php
$ch = curl_init();
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, true);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_URL, 'https://api-testnet.bitcoin-balance-api.com/v1/address/tb1qlw09ycnp3qgqw9alqgx93ed7cg5kmnyud326ky');
$result = curl_exec($ch);
curl_close($ch);

$obj = json_decode($result);
echo 'Bitcoin Balance: ' . $obj->balance;
?>
```
