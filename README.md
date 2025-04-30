##  Simple Image Encryption Tool
This is a lightweight Python-based tool that allows you to encrypt and decrypt images using basic pixel manipulation. It's a great way to understand how simple reversible transformations can obscure visual data.

# 📌 Features
🔒 Encrypt images by modifying pixel RGB values with a key.

🔓 Decrypt images using the same key to restore the original.

🖼️ Supports popular image formats like JPG, PNG, and BMP.

🧩 Simple CLI interface using argparse.

# 🧠 How It Works
Each pixel's RGB values are adjusted using a key:

## Encryption:

python
Copy
Edit
(r + key) % 256
## Decryption:

python
Copy
Edit
(r - key + 256) % 256
Since the operations are reversible, the original image can be perfectly restored if the same key is used.

📦 Requirements
Python 3.x

Pillow (PIL)

# Install dependencies:

bash
Copy
Edit
pip install pillow
🚀 Usage
Run the script from the command line:

# 🔐 Encrypt an Image
bash
Copy
Edit
python encryptor.py encrypt --input path/to/input.jpg --output path/to/encrypted.png --key 123
# 🔓 Decrypt an Image
bash
Copy
Edit
python encryptor.py decrypt --input path/to/encrypted.png --output path/to/decrypted.jpg --key 123
Make sure to use the same key for encryption and decryption!
