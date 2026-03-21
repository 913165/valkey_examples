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
chmod 777 *
tar -xzvf ./valkey-9.0.3-noble-x86_64.tar.gz
chmod 777 *
cd valkey-9.0.3-noble-x86_64
cp bin/valkey-server /usr/local/bin/
cp bin/valkey-cli /usr/local/bin/
```

# check valkey version
```
valkey-server --version
```

# to start valkey server just execute below command

``
valkey-server 
```

# to start with valkey-cli go to another terminal and try below command

```
valkey-cli
```
