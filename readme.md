# Simple crypto

Implements;

    { encrypt(string): string ; decrypt(string): string }

from passphrase with aes-128-cbc

Install:

    yarn add @australis/tiny-crypto

Usage:

    import Crypto from "../src";
    import { randomBytes } from "crypto";

    const secret = randomBytes(10).toString("base64");    
    const crypto = new Crypto(secret);
    console.log(crypto.decrypt(crypto.encrypt("hello")));
    # should print hello

