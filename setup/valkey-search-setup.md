# valkey-search-setup.md
Quick Start
https://github.com/valkey-io/valkey-search/blob/main/QUICK_START.md
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

# git clone below site

```
git clone https://github.com/valkey-io/valkey-search.git
cd valkey-search
```

https://github.com/valkey-io/valkey-search/tree/main?tab=readme-ov-file#build-instructions


Install basic tools
Ubuntu / Debian
```
sudo apt update
sudo apt install -y clangd          \
                    build-essential \
                    g++             \
                    cmake           \
                    libgtest-dev    \
                    ninja-build     \
                    libssl-dev      \
                    clang-tidy      \
                    clang-format    \
                    libsystemd-dev
```
# run below command 
```
./build.sh
```
