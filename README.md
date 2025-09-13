# ProVerif Implementation of "A Lightweight and Secure Extended AKA Protocol for Direct-to-Cell LEO Satellite Constellations"

This repository contains the **ProVerif** formal verification code for the extend authentication and key agreement (eAKA) protocol proposed in the paper:

> **"A Lightweight and Secure Extended Authentication and Key Agreement Protocol for Direct-to-Cell LEO Satellite Constellations"**

The protocol is designed for secure and efficient mobile users authentication and session key establishment in direct-to-cell low Earth orbit (LEO) satellite communication systems. This ProVerif implementation verifies the security properties of the protocol under the **Dolev-Yao threat model**.

---

## 🔍 Verified Security Properties

The following security properties have been formally verified using ProVerif:

- ✅ **Secrecy of the group key and session key**  
  Ensures that the negotiated keys remain confidential against active attackers.

- ✅ **Authenticity of bootstrapping messages**  
  Confirms that system parameters (e.g., MIB/SIBs) are signed and authenticated by the legitimate satellite.

- ✅ **Mutual authentication between satellite and mobile users (MUs)**  
  Guarantees that both the satellite and users can authenticate each other during the AKA process.

---

## 📁 Repository Structure
.
├── Protocol.pv           # Main ProVerif code: protocol model and security queries
└── README.md             # This file


- `Protocol.pv`: The core ProVerif script defining:
  - Cryptographic primitives (signatures, hash functions, etc.)
  - Protocol roles (Satellite, Mobile User, CN )
  - Message flows
  - Security queries (secrecy, authentication)

---

## 🛠️ How to Run

### Prerequisites

- [ProVerif]([https://bblanche.gitlabpages.inria.fr/proverif/proverif2.05.tar.gz]) (version 2.05)


### Steps

1. **Install ProVerif**  
   Follow installation instructions at: [https://bblanche.gitlabpages.inria.fr/proverif/manual.pdf]

2. **Run the verification**  
   Execute the following command in your terminal:

   ```bash
   proverif protocol.pv
