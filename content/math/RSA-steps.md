+++
title = "A Basic Implementation of RSA"
date = 2023-11-23T00:00:52-07:00
tags = ["math"]
+++


### Introduction

This is the general steps needed to implement an extremely basic form of RSA from my understanding

RSA is an encryption algorithm that finds numbers **n**, **d**, **e** where **m** mod **n** ≡ (**m**^**e**)^**d** mod **n**. With **m** being the plaintext message and **c** being the cipher text, **n** and **e**, the public key, are released. This means anybody can encrypt a message with  **c** = **m**^**e** mod **n** and decrypt it using **m** = **c**^**d** mod **n**. 

**n** is made by multiplying two primes and it's secure since it's hard to factor large primes with classical computers. This lets you release **n** without having them know which primes you used and those primes are then used to generate **d**, the private key.


This means RSA is secure against brute force attacks if you make **n** really large and take some precautions to make it so people can't guess which primes are used. I don't fully know what issues there are, but a simple example that's true in the right situation is if you have a twin prime (11 and 13 lets say) they can take the square root and get a good estimate since taking square roots is really fast. 

Steps with an * will have a note at the end if there's an issue with the basic implementation for practical usage.

### Step 1, Primes*
Randomly generate 2 primes, **p1** and **p2**. Keep **p1** and **p2** secret.

### Step 2, n
Find **p1** \* **p2**, **n**.

### Step 3, phi*
Find the number of integers relatively prime to **n**, **phi**, using Euler's totient function, which is (**p1**-1)(**p2**-1). Keep **phi** secret.

### Step 4, e (not that e)*
Find an integer **e** which is coprime with **phi**. This is when 2\<**e**\<**phi**-1 and gcd(**e**,**phi**)=1.

### Step 5, The private key*
Find the private key exponent, **d**, which is the modular inverse of **e** mod **phi**. This is the number where **e** \* **d** mod **phi** = 1 and can be implemented by checking each number from 1 to **phi** until this is true.

### Step 6, The public key
This is just **n** and **e**.

### Encrypting a message (with the public key)
1. Split the message into an array, **u_array**
2. Convert each element of **u_array** to a number, **u** (I used the unicode code)
3. Find **u**^**e** mod **n** for each element. The resulting array will consist of each character encrypted using the public key. 
4. You can turn this into a string, but I'm not sure how to split it up again. 
5. Release the public key along with the resulting array/string

### Decrypting a message (with the private key)
1. For each element **u** in **u_array**, find **u**^**d** mod **n**. The resulting number will be the numerical representation of the character (the unicode code of each character)
2. Convert this code back to a character
3. Combine the array into a string

---
### \*1
**p1** and **p2** should be very large and have a large difference. This makes it so it's really hard to find which primes made up **n** since **n** will be public. 

### \*3
Carmichael's totient function, **lambda**, is used in modern implementations, which is lcm(**p1**-1, **p2**-1), since I think it's more performant than **phi** since with **phi** the private exponent, **d**, could be larger than necessary.

### \*4
**e** should have a short bit-length and Hamming weight (no idea what that does) and is generally 2^16 + 1 = 65537 since it's released with the public key, so it can be known.

### \*5
Obviously the method used for the modular inverse is as slow as possible so something called the extended Euclidean algorithm is used to find it. 
