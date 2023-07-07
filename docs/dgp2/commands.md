# Metrix DGP Command Glossary

This glossary of commands describes common DGP calls using the debug or CLI consoles.


## getdgpinfo
This command will output the current DGP info at the currently syncronised block height.


#### Command

```
getdgpinfo
```

#### Output

```
{
  "maxblocksize": 2000000,
  "mingasprice": 5000,
  "blockgaslimit": 40000000,
  "minrelaytxfee": 1000000000,
  "incrementalrelayfee": 1000000000,
  "dustrelayfee": 3000000000,
  "governancecollateral": 750000000000000,
  "budgetfee": 60000000000000,
  "contracts": {
    "version": 2,
    "dgp": "a523bfd08ca0365ca0f93de522c8d53590447a52",
    "governance": "13a5933a1b786e8016178656145e36eccd0221f6",
    "budget": "28238c7d116aa2ca3739c4c93038fd5a06a77303"
  }
}
```
