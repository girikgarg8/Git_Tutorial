Git internally uses :

1. Hashing
2. Graph/Tree Data Structure

==> Git is like key-value store.

Key used is the hash of the data and value is the data.

git uses a cryptographic hash function -> SHA1 (Secure Hash Algorithm 1)

For a given data, it outputs 40 digit hexadecimal number. The hash value is always same for same data.

git compresses the data in a blob (binary large object), and stores some metadata about data.

Structure of how git stores the data:

![Git internal memory representation](Internal_Git_Representation.png)