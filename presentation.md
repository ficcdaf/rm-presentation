[comment]: # "THEME = black"
[comment]: # "CODE_THEME = base16/zenburn"
[comment]: # "controls: true"
[comment]: # "keyboard: true"
[comment]: # "markdown: { smartypants: true }"
[comment]: # "hash: false"
[comment]: # "respondToHashChanges: false"

# Defeating Real-Time Phishing with Sound-Based Authentication

Daniel Fichtinger, MSc. Candidate

Supervisors: Dr. Furkan Alaca & Dr. Mohammed Zulkernine

[comment]: # "!!!"

## What Is Authentication?

[comment]: # "!!! data-auto-animate"

## What Is Authentication?

- Bob **claims** to be Bob.

[comment]: # "!!! data-auto-animate"

## What Is Authentication?

- Bob **claims** to be Bob.
- Alice asks Bob for **proof**.

[comment]: # "!!! data-auto-animate"

## What Is Authentication?

- Bob **claims** to be Bob.
- Alice asks Bob for **proof**.
- Alice **verifies** the proof.

[comment]: # "!!! data-auto-animate"

## What Is Authentication?

- Bob **claims** to be Bob.
- Alice asks Bob for **proof**.
- Alice **verifies** the proof.
- ∴ Alice **authenticates** Bob.

[comment]: # "!!! data-auto-animate"

## Types Of Authentication

### Knowledge

What you know.

[comment]: # "!!! data-auto-animate"

## Types Of Authentication

### Possession

What you have.

[comment]: # "!!! data-auto-animate"

## Types Of Authentication

### Inherence

What you are.

[comment]: # "!!! data-auto-animate"

## Why aren't passwords good enough?

Imagine the following scenarios:

- Data breach → Password theft
- Weak password → Password guessing

[comment]: # "!!!"

## Phishing

Attacker steals a password by _tricking_ the user into typing it in on a **fake website** that _looks_ real.

[comment]: # "!!!"

## Multi Factor Authentication

- Combines **Knowledge** and **Possession**
  - Vulnerable to real-time phishing
    - **RTP**: _Both factors are phished at once, in real-time._

[comment]: # "!!!"

## Passwordless Authentication

- Combines **Inherence** and **Possession**
  - **FIDO**: The crown jewel of pw-less authentication.
  - Not vulnerable to **real-time phishing**.
    - The private key is _impossible to intercept_ as it never **leaves** the device.
  - Other attacks possible.

[comment]: # "!!!"

## Sound-Proof

A unique, _sound-based_ MFA protocol.

[comment]: # "!!!"

### Client-Server Implementation

[comment]: # "!!!"
[comment]: # '!!! data-background-image="media/Soundproof-Page-1.svg" data-background-size="contain"'

### Peer-to-Peer Implementation

[comment]: # "!!!"
[comment]: # '!!! data-background-image="media/Soundproof-Page-2.svg" data-background-size="contain"'

### Microphone-Spoofing Phishing Attack

_An attack designed by me. To the best of my knowledge, it is **novel**._

[comment]: # "!!!"
[comment]: # '!!! data-background-image="media/cringe.svg" data-background-size="contain"'
[comment]: # '!!! data-background-image="media/Soundproof-Page-3.svg" data-background-size="contain"'

## Related Papers

[comment]: # "!!!"

### Sound-Proof

N. Karapanos, C. Marforio, C. Soriente, and S. Capkun, “{Sound-Proof}: Usable {Two-Factor} Authentication Based on Ambient Sound,” presented at the 24th USENIX Security Symposium (USENIX Security 15), 2015, pp. 483–498. Accessed: Nov. 19, 2024. \[Online\]. Available: https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/karapanos

[comment]: # "!!!"

### SoundID

D. Liu et al., “SoundID: Securing Mobile Two-Factor Authentication via Acoustic Signals,” IEEE Transactions on Dependable and Secure Computing, vol. 20, no. 2, pp. 1687–1701, Mar. 2023, doi: 10.1109/TDSC.2022.3162718.

[comment]: # "!!!"

## Research Objective

- To investigate whether:
  - A Sound-Based authentication protocol can resist phishing.
- If so:
  - Does it provide a security benefit over FIDO?

[comment]: # "!!!"

## Research Questions

- **RQ1**: Does the phishing attack against the peer-to-peer Sound-Proof protocol require more complexity than the phishing attack against the server-client protocol?
  - Are they different attacks?
  - Will the same defense work against both?

[comment]: # "!!! data-auto-animate"

## Research Questions

<div style="font-size: 0.5em;">

- **RQ1**: Does the phishing attack against the peer-to-peer Sound-Proof protocol require more complexity than the phishing attack against the server-client protocol?

</div>

- **RQ2**: Is the only way to address the phishing problem by converging towards the FIDO protocol?
  - Can we stop the attack _without_ relying on a **secure local channel** (hallmark of FIDO)?

[comment]: # "!!! data-auto-animate"

## Research Questions

<div style="font-size: 0.5em;">

- **RQ1**: Does the phishing attack against the peer-to-peer Sound-Proof protocol require more complexity than the phishing attack against the server-client protocol?
- **RQ2**: Is the only way to address the phishing problem by converging towards the FIDO protocol?

</div>

- **RQ3a**: If a non-FIDO solution exists, then what makes sound a good defense against phishing?
  - Does the sound mechanism grant a unique security characteristic?

[comment]: # "!!! data-auto-animate"

## Research Questions

<div style="font-size: 0.5em;">

- **RQ1**: Does the phishing attack against the peer-to-peer Sound-Proof protocol require more complexity than the phishing attack against the server-client protocol?
- **RQ2**: Is the only way to address the phishing problem by converging towards the FIDO protocol?
- **RQ3a**: If a non-FIDO solution exists, then what makes sound a good defense against phishing?

</div>

- **RQ3b**: If only a FIDO solution exists, then does adding sound **improve** on FIDO?

[comment]: # "!!! data-auto-animate"

## Methodology

[comment]: # "!!!"

### RQ1: Is the P2P attack more complex?

1. Prove that my attack is novel.
2. Map out both versions of the attack.
3. Compare their complexity.
4. Implement the attack to prove that it works.

[comment]: # "!!!"

### RQ2: Is the FIDO way the only way?

1. Enumerate possible improvements to the protocol that do **not** converge towards FIDO.
2. If one is found, implement to prove its validity.

[comment]: # "!!!"

### RQ2: Is the FIDO way the only way?

1. If not found, repeat the same process, find an improved protocol that **does** converge towards FIDO.
2. Implement to prove its validity.

[comment]: # "!!!"

### RQ3a: What makes sound a good defense against phishing?

#### If a non-FIDO solution exists:

- Implement an attack that:
  - Works against another MFA scheme.
  - **Doesn't** work against the sound scheme.

[comment]: # "!!!"

### RQ3b: How does sound improve FIDO?

#### If only a FIDO solution exists:

- Implement an attack that:
  - Works against FIDO.
  - **Doesn't** works against the sound scheme.

[comment]: # "!!!"

## In Conclusion

If security is bad, hackers win.

My research aims to make security better, so hackers lose.

Thank you!
