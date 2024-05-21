# Notes

1. When we XOR ciphertexts, we get the XOR-ed value of the original texts.
2. The last ciphertext is all 0s, which suggests that it the result of the key XOR-ing with itself. Consequently, the last ciphertext is the key itself.

## Approach

Do simple frequency analysis. Plaintext XORs with valid alphabets usually have values less than 26 for each byte. Brute force on some crib-drag tools online https://toolbox.lotusfa.com/crib_drag/.

## Plaintexts

1. The Times 03/Jan/2009 Chancellor on brink of second bailout for banks.
2. Governments are good at cutting off the heads of a centrally controlled networks like Napster, but pure P2P networks like Gnutella and Tor seem to be holding their own.
3. Bitcoin is great as a form of digital money, but its scripting language is too weak for any kind of serious advanced applications to be built on top.
4. In order to have a decentralized database, you need to have security. In order to have security, you need to have incentives.
5. As society becomes more and more complex, cheating will in many ways become progressively easier and easier to do and harder to police or even understand.
6. I began to realize new possibilities opening up between the fields of ICT and game theory, and the inevitable social change to which this would lead.
7. Cryptocurrencies allowed non-custodial exchange, without users having to sign up or create accounts.
8. Not your keys, Not your coins.

## Key

Bitcoin: A purely peer-to-peer version of electronic cash would allow online payments to be sent directly from one party to another without going through a financial institution

## Additional Challenge

In the ciphertext, we notice that there are many duplicates of the 3 hexadecimal characters '1f3', between every 2 characters in the start and end of the string. This could indicate that the characters were intentionally added to obfuscate the ciphertext even more. Luckily, removing these characters allow us to use the same key as before to decrypt.

Original Ciphertext: 1f3cb1f3e01f3fd1f3ea1f3e61f3e01f3e71f3b31f3a91f3c81f3a91f3f91f3fc1f3fb1f3ec1f3e51f3f01f3a91f3f91f3ec1f3ec526e1b014a020411074c17111b1c071c4e4f0146430d0d08131d1d010707040017091648461e1d0618444f074c010e19594f0f1f1a07024e1d041719164e1c1652114f411645541b004e244f080213010c004c3b4c0911040e480e070b00310213101c4d0d4e00360b4f151a005253184913040e115454084f010f114554111d1a550f0d520401461f3e01f3e71f3e81f3e71f3ea1f3e01f3e81f3e51f3a91f3e01f3e71f3fa1f3fd1f3e01f3fd1f3fc1f3fd1f3e01f3e61f3e71f3a7

Cleaned Ciphertext: cbe0fdeae6e0e7b3a9c8a9f9fcfbece5f0a9f9ecec526e1b014a020411074c17111b1c071c4e4f0146430d0d08131d1d010707040017091648461e1d0618444f074c010e19594f0f1f1a07024e1d041719164e1c1652114f411645541b004e244f080213010c004c3b4c0911040e480e070b00310213101c4d0d4e00360b4f151a005253184913040e115454084f010f114554111d1a550f0d52040146e0e7e8e7eae0e8e5a9e0e7fafde0fdfcfde0e6e7a7

Decrypted Text:
 Congratulations on championing the first of many assignments here at the Polkadot Blockchain Academy! We are so glad to have you here! 
