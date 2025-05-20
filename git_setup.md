# 🚀 How to Install and Set Up Git with SSH

## 📥 Step 1: Download Git

Download Git for your system (Windows, Linux, or macOS) from the official website:

👉 [Download Git](https://git-scm.com/downloads)

---

## 🔗 Step 2: Clone Repositories – HTTPS vs SSH vs GitHub CLI

You can clone repositories using:
- **HTTPS**
- **SSH**
- **GitHub CLI**

> ✅ I prefer **SSH** — it's secure and avoids repeated username/password prompts.

---

## 🔐 What is SSH?

**SSH (Secure Shell)** is a secure protocol used to connect to remote computers and servers using cryptographic key pairs instead of passwords.

---

## 🔑 Step 3: Generate and Add SSH Key to GitHub

Use the **`ed25519`** algorithm — modern, fast, and secure, over **`RSA`**

### 🛠️ Follow below Commands to Generate SSH Key

> ⚠️ **Note:** If you're on Windows, use **Git Bash** or **WSL** for a smoother experience.

```bash
# Open terminal and run this command (replace with your GitHub email)
ssh-keygen -t ed25519 -C "your_email@example.com"

# This creates key pair in ~/.ssh/ (id_ed25519 and id_ed25519.pub)
# When prompted, press Enter to save in the default location.

# Add the SSH key to SSH agent to avoid enter passphrase if setup already during keygen
ssh-add ~/.ssh/id_ed25519

# Copy the public key and add to github SSH keys (you will find in profile settings)
cat ~/.ssh/id_ed25519.pub


