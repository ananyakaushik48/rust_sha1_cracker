# SHA1 Cracker

A simple Rust-based SHA1 hash cracker from the black-hat-rust (repo)[https://github.com/skerkour/black-hat-rust/tree/main] that attempts to reverse a SHA1 hash using a wordlist. This program is a demonstration of how hash cracking works and is intended for educational purposes only.

---

## Features
- Takes a SHA1 hash and a wordlist as inputs.
- Compares the hash against SHA1 hashes of words in the wordlist.
- Outputs the matched password if found.

---

## Usage

### Prerequisites
- Install [Rust](https://www.rust-lang.org/tools/install).
- Ensure you have a wordlist file (e.g., `wordlist.txt`) and a SHA1 hash to crack.

### Build
Clone the repository and build the program using Cargo:
```bash
git clone https://github.com/ananyakaushik48/sha1-cracker.git
cd sha1-cracker
cargo build --release
```

### Run
Run the program with the wordlist and hash as arguments:
```bash
./target/release/sha1_cracker <wordlist.txt> <sha1_hash>
```

Example:
```bash
./target/release/sha1_cracker wordlist.txt 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8
```

Expected output (if the password exists in the wordlist):
```plaintext
Password found: password
```

---

## Wordlist Example

Here’s an example of a `wordlist.txt` file:

```
password123
123456
admin
letmein
welcome
iloveyou
monkey
football
princess
qwerty
```

You can use this or any other wordlist for testing.

---

## Example SHA1 Hashes

Here’s a sample of SHA1 hashes you can test with:

| Password   | SHA1 Hash                                           |
|------------|-----------------------------------------------------|
| password   | 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8            |
| 123456     | 7c4a8d09ca3762af61e59520943dc26494f8941b            |
| admin      | d033e22ae348aeb5660fc2140aec35850c4da997            |
| letmein    | 0d107d09f5bbe40cade3de5c71e9e9b7                    |

Download the full example files:
- [wordlist.txt](wordlist.txt)
- [SHA1 hashes CSV](sha1_hashes.csv)

---

## Error Handling
- If the input SHA1 hash is invalid (not 40 characters), the program will return an error.
- If the password is not found in the wordlist, it will print:
  ```plaintext
  password not found in wordlist :(
  ```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Disclaimer

This tool is for educational purposes only. Do not use it for unauthorized or illegal activities.


