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
# after completing build

```
cd  /home/tinumistry/valkey-9.0.3-noble-x86_64/valkey-search/.build-release
valkey-server --loadmodule /home/tinumistry/valkey-9.0.3-noble-x86_64/valkey-search/.build-release/libsearch.so
```

# after done open another terminal and goti site and try  Step 3: Create a Vector Index
https://github.com/valkey-io/valkey-search/blob/main/QUICK_START.md

```
valkey-cli
FT.CREATE myIndex SCHEMA vector VECTOR HNSW 6 TYPE FLOAT32 DIM 3 DISTANCE_METRIC COSINE
HSET my_hash_key_1 vector "\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x80?"
HSET my_hash_key_2 vector "\x00\xaa\x00\x00\x00\x00\x00\x00\x00\x00\x80?"
FT.SEARCH myIndex "*=>[KNN 5 @vector $query_vector]" PARAMS 2 query_vector "\xcd\xccL?\x00\x00\x00\x00\x00\x00\x00\x00"
```
