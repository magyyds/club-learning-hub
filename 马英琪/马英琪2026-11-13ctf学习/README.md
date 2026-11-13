# 2026-11-13 CTF实战记录

今天听取了学长的建议，不再盲目铺开，主要聚焦于 Crypto（密码学）和 Misc 的实战打靶。

## 一、 CTFshow 平台实战（Crypto）
1. **键盘密码（萌新_密码2）**：通过观察按键在键盘上的包围位置，成功解出 `KEY{fwy}`。
2. **十六进制+Base64+栅栏密码（萌新_密码1）**：在终端使用 `echo "..." | xxd -r -p` 和 `base64 -d` 命令行连招硬解，配合 CyberChef 的 Rail Fence 解密，拿下 `KEY{dffb6a33...}`。
3. **摩斯密码+培根密码（萌新_密码3）**：利用 CyberChef 的 `From Morse Code` 和 `Bacon Cipher Decode`，经过多次 M/D 替换与反转测试，解出 `flag{GUOWANG}`。这题深刻体会到了出题人密文长度有误时的排查过程。

## 二、 Misc 隐写实操
1. 学习了 ZIP 伪加密的原理。
2. 在终端中尝试用 Python 脚本修改 `PK\x03\x04` 标志位来绕过密码限制。
3. （萌新_隐写2 环境被我改坏了，暂时搁置，但掌握了 `file` 和 `strings` 三板斧的底层逻辑）。

## 三、 工具与技能沉淀
- 熟练使用 CyberChef 处理多种古典密码。
- 掌握了 Mac 终端原生命令 `xxd` 和 `base64` 直接解码。
