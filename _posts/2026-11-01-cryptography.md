---
layout: post
title: "cryptography"
---

## 分组加密和流加密

- 分组加密将明文按固定长度分成若干组，主要有DES，AES（固定分组长度是 128 位）

- 流加密逐位或逐字节加密，主要有RC4（已弃用）、ChaCha20、Salsa20



使用AES可以构造流加密模式，比如aes-256-cfb

256代表密钥长度为256位（32字节）

cfb表示Cipher Feedback（密文反馈）的工作模式，使用cfb就可以用分组密码构造流加密模式

## AES-CFB和AES-GCM的区别
本质就是工作模式的区别
使用gcm可以除了可以提供机密性，还可以提供完整性认证

gcm属于AEAD（认证加密）
