# JWT cracker

A JWT brute-force cracker written in C.

I used the [Apple Base64 implementation](https://opensource.apple.com/source/QuickTimeStreamingServer/QuickTimeStreamingServer-452/CommonUtilitiesLib/base64.c) that I modified slightly.

## Compile

Make sure you have openssl's headers installed.

```
make
./jwtcrack eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.cAOIAifu3fykvhkHpbuhbvtH807-Z2rI1FS3vX1XMjE
```

In the above example, the key is `Sn1f`. It takes approximately 2 minutes to crack on my Macbook.

## Caveats

 * Not multi-threaded :((
 * Letters permutation generator could be a bit faster :|
 * No progress status :(
 * If you stop the program, you cannot start back where you were :((
