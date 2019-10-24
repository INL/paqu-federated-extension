This is an adapter that allows [PaQu](https://github.com/rug-compling/paqu) to communicate with the [gretel 4] frontend.
It must be compiled into PaQu.

```bash
git clone https://github.com/rug-compling/paqu -b master
git clone https://github.com/INL/paqu-federated-extension -b master
cp paqu-federated-extension/*.go paqu/src/pqserve/

# now compile paqu as you normally would
```

Add the following to the gretel configuration files:  
web-ui/src/assets/config/config.*.json
```json
{
    "providers": {
        "paqu": "path.to.host:port/api/gretel/"
    }
}
```
