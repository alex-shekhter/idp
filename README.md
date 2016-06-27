# Identity Provider (IdP) for Hydra [![Build Status](https://travis-ci.org/janekolszak/idp.svg?branch=master)](https://travis-ci.org/janekolszak/idp)

**Under development**

If you're looking for an example IdP integration with Hydra - it's [here](https://github.com/janekolszak/hydra-idp-go).


## About
Writing a general, all purpose Identity Provider is beyond me. 
Instead I want to provide this little playground with different tools that you can use to create your own ideal IdP.


## Running the example:
#### Console 1:
Start Hydra and browse it's logs. Copy the client's credentials, you'll need them in Console 3.
``` bash
cd example
docker-compose up hydra
```

#### Console 2:
Start IdP and browse it's logs
``` bash
cd example
docker-compose up idp
``` 

#### Console 3
Perform some experiments like:
``` bash
# Pass the credentials from Console 1
hydra connect
hydra token user --skip-tls-verify --no-open
# Paste the link to Firefox
```

## TODO:
- Displaying scopes
- Login/Logout endpoint
- Digest Auth Provider
- Form Provider
- API for getting keys from Hydra
- Encrypting cookies
- Trusted clients that won't trigger asking user to agree upon scopes
