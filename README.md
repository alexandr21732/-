Описание:
Этот модуль предназначен для шифрования и дешифрования данных с использованием алгоритма RSA. В основе реализации лежит библиотека cryptography.

Возможности:
- Генерация пары ключей RSA (закрытый и открытый).
- Шифрование текстовых сообщений с помощью открытого ключа.
- Дешифрование данных с помощью закрытого ключа.
- Использование OAEP (Optimal Asymmetric Encryption Padding) с хешированием SHA-256.

▌ Требования

Для работы модуля установите библиотеку cryptography:

pip install cryptography

▌ Использование

▌ 1. Генерация ключей

private_key, public_key = generate_keys()

▌ 2. Шифрование сообщения

ciphertext = encrypt_data(public_key, "Привет, мир!")

▌ 3. Дешифрование сообщения

plaintext = decrypt_data(private_key, ciphertext)
print(plaintext)  # Привет, мир!

▌ Функции

▌ generate\_keys()

Генерирует пару ключей RSA: закрытый и открытый.
Возвращает:

- private_key — закрытый ключ.
- public_key — открытый ключ.

▌ encrypt\_data(public\_key, message: str) -> bytes

Шифрует строку message с использованием открытого ключа public_key.
Возвращает зашифрованные данные в виде байт.

▌ decrypt\_data(private\_key, ciphertext: bytes) -> str

Дешифрует байты ciphertext с использованием закрытого ключа private_key.
Возвращает исходную строку.
