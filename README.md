# COSE Signing Prototype in JavaScript

This is a simple prototype demonstrating COSE (CBOR Object Signing and Encryption) signing and verification operations implemented in JavaScript. It uses the Web Crypto API and CBOR encoding, packaged in a single HTML file for easy testing and exploration.

## Features

- Generate ECDSA P-256 key pair using the browser’s Web Crypto API
- Create a COSE_Sign1 message signing a JSON payload
- Verify the COSE_Sign1 signature using the generated public key
- Display keys, payload, signed message, and verification status in the UI
- Fully client-side, runs in any modern browser (no backend)
- Mobile responsive and visually clean interface

## How to Use

1. Open the `cose-signing-prototype.html` file in a modern browser (Chrome, Firefox, Edge, Safari).
2. Click **Generate ECDSA P-256 Key Pair** to create a new signing key pair.
3. Modify the JSON payload in the text area if desired.
4. Click **Sign Payload** to generate a COSE_Sign1 signature of the payload.
5. The COSE signed message will be displayed as a Base64-url encoded string.
6. Click **Verify Signature** to validate the signature against the public key.
7. See the verification status below the button.

## Technologies Used

- [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API) for key generation, signing, and verifying
- [CBOR (Concise Binary Object Representation)](https://datatracker.ietf.org/doc/html/rfc7049) for structured binary encoding, via open-source CBOR JS library
- Pure client-side JavaScript with no external dependencies except CBOR library for encoding/decoding

## COSE Background

This prototype implements the COSE_Sign1 structure as defined in [RFC 8152](https://datatracker.ietf.org/doc/html/rfc8152), which specifies how to apply cryptographic signatures using CBOR encoding. The signing algorithm used here is ECDSA with curve P-256 and SHA-256 hashing (COSE alg `ES256`).

## Notes

- The key pair is generated fresh on each page load or button press — keys are not persisted.
- The prototype supports only a basic COSE_Sign1 signing/verification workflow without external authentication or encrypted content.
- Payload input expects valid JSON text.
- Code and UI are optimized for mobile devices with max width 350px and max height 600px but work on desktop as well.

## License

This project is provided for educational and prototyping purposes without any warranty. Use and modify freely.

---

Feel free to explore and extend this prototype to incorporate more COSE features, such as encryption, multi-signatures, or different algorithms!

