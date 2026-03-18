# goto site
```
https://valkey.io/
```

# download file
```
wget https://download.valkey.io/releases/valkey-9.0.3-noble-x86_64.tar.gz
```

# extract and setup valkey
```
 tar -xzvf ./valkey-9.0.3-noble-x86_64.tar.gz
cd valkey-9.0.3-noble-x86_64
cp bin/valkey-server /usr/local/bin/
cp bin/valkey-cli /usr/local/bin/
```

# check valkey version
```
valkey-server --version
```
