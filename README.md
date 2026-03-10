# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
```
def power(a, b, P):
    if b == 1:
        return a
    else:
        return (a ** b) % P

def main():
    print("\n***** Diffie-Hellman Key Exchange Algorithm *****\n")

    P = int(input("Enter the value of P: "))
    print(f"The value of P: {P}")

    G = int(input("Enter the value of G (Primitive root of P): "))
    print(f"The value of G: {G}\n")

    a = 4
    print(f"The private key a for ilevarasen: {a}")
    x = power(G, a, P)

    b = 3
    print(f"The private key b for arasen: {b}\n")
    y = power(G, b, P)

    ka = power(y, a, P)
    kb = power(x, b, P)

    print(f"Secret key for ilevarasen is : {ka}")
    print(f"Secret key for arasen is : {kb}")

main()
```


## Output:
<img width="1240" height="399" alt="image" src="https://github.com/user-attachments/assets/88d4f36b-1b19-4b78-965a-0d817bff72a1" />

## Result:
  The program is executed successfully.
