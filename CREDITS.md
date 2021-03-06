# Credits, Notes, and Reference

## Narmi API

  + https://www.narmi.com/developers/guides/

This curl request works using demo credentials (use your own token and secret):

```sh
token='________________'
secret='________________'
date=`date -u +'%Y-%m-%dT%H:%M:%SZ'`

signature=`echo -n "date: $date" | openssl dgst -sha256 -binary -hmac "$secret" | base64`

curl -H "Authorization: Bearer $token" -H "Date: $date" -H "Signature: keyId=\"$token\",algorithm=\"hmac-sha256\",headers=\"date\",signature=\"$signature\"" 'https://api.demo.narmitech.com/v1/accounts/'

# also works:
curl https://api.demo.narmitech.com/v1/accounts/ -H "Authorization: Bearer $token" \
    -H "Date: $date" \
    -H "Signature: keyId=\"$token\",algorithm=\"hmac-sha256\",headers=\"date\",signature=\"$signature\""
```

## Narmi Banking Client Package

  + https://github.com/narmitech/banking-client-python
  + https://github.com/narmitech/banking-client-python/blob/c51d2c9c469dbd6ca50c814c0ff98b93c57198e5/banking_client/api/account_api.py#L259-L283
  + https://github.com/narmitech/banking-client-python/blob/c51d2c9c469dbd6ca50c814c0ff98b93c57198e5/banking_client/api/account_api.py#L285-L370
  + https://github.com/narmitech/banking-client-python/blob/c51d2c9c469dbd6ca50c814c0ff98b93c57198e5/banking_client/api_client.py#L284-L342

Doesn't import?

  + https://github.com/narmitech/banking-client-python/issues/1

## Requests Package

  + http://docs.python-requests.org/en/master/user/quickstart/
  + https://stackoverflow.com/questions/6260457/using-headers-with-the-python-requests-librarys-get-method

## System Calls

  + https://stackoverflow.com/a/4256153/670433
  + https://github.com/prof-rossetti/repo-evaluator-py/blob/6cf3030967ddaea7eebc3204b8587408a53104e6/app/repo_downloader.py#L5-L14
  + https://stackoverflow.com/questions/89228/calling-an-external-command-in-python
