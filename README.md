# 🧬 GitHub Streak Keeper

Keep your GitHub streak alive automatically with a simple GitHub Action that commits daily to this repo. Works on **both public and private** repositories.

---

## 🚀 Features
- ⏰ Automatically commits **twice a day** (morning & evening)
- 🔒 Uses **Personal Access Token (PAT)** for secure authentication
- 🧑‍💻 Non-intrusive: only updates a dummy file

---

## 📦 How to Use

### 1. **Fork this repo**
Click ⭐ then Fork this repository to your account.

### 2. **Generate a Personal Access Token (PAT)**
1. Go to [Settings → Developer Settings → Personal Access Tokens → Fine-grained tokens](https://github.com/settings/personal-access-tokens)
2. Click **Generate new token**
3. Select the **target repository** (e.g. `your-username/streak-keeper`)
4. Under **Permissions**, enable:
   - ✅ **Contents** → Read and Write
   - ✅ **Actions** → Read and Write (optional but recommended)
5. Copy the token (you'll need it later).

### 3. **Add the token to GitHub Secrets**
1. Open your forked repo
2. Navigate to **Settings → Secrets and variables → Actions**
3. Click **New repository secret**
   - **Name:** `GH_PAT`
   - **Value:** (paste your token here)

### 4. ✅ All set!
The GitHub Action will now run automatically every day at **06:00 WIB (UTC + 7)** and **18:00 WIB(UTC + 7)** 🚀

---

## 🧠 How It Works
The workflow:
1. Checks out the repo
2. Appends a line to `keepalive.txt`
3. Commits with message `chore: keep streak alive`
4. Pushes the changes using your PAT

---

## ❓ FAQ
**Is this secure?**
> ✅ Yes! Your PAT is stored as a secret and never exposed publicly

**Can I use this on a private repo?**
> ✅ Absolutely. Just ensure your PAT has `repo` access

**Does this count toward GitHub streaks?**
> ✅ Yes, as it creates a valid commit and push

---

## 💖 Credits
Made with ❤️ by [@arsybai](https://github.com/arsybai) & Akari ✨
