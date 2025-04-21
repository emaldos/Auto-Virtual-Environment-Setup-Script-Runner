# ⚙️ Auto Virtual Environment Setup & Script Runner

This Python script automates:

- ✅ Creating a virtual environment  
- 📦 Installing dependencies from a `.txt` file  
- 🚀 Running another Python script as a background (detached) process  
- 🧪 Running basic unit tests  
- 🔍 Dry‑run mode for safe simulation  

---

## 📁 Project Structure

```text
your_project/
├── run_auto_setup.py               # This automation script
├── your_script.py                  # The target script to run
├── requirements.txt                # (Optional) List of libraries to install
```

---

## 🧰 Requirements

- Python 3.x  
- Works on **Linux**, **macOS**, and **WSL**  

---

## ▶️ Usage Examples

### 1. Basic Run

```bash
python3 run_auto_setup.py -f your_script.py
```

- Creates `myenv/` if missing  
- Skips library installation  
- Launches `your_script.py` detached  

---

### 2. With Libraries

```bash
python3 run_auto_setup.py -f your_script.py -l requirements.txt
```

- Installs every package listed in `requirements.txt`  
- Then launches your script  

---

### 3. Passing Extra Arguments

```bash
python3 run_auto_setup.py -f your_script.py -l requirements.txt --extra --port 8080 --debug
```

- Everything after `--extra` is forwarded to `your_script.py`  

---

### 4. Force Re‑creation

```bash
python3 run_auto_setup.py -f your_script.py --force
```

- Deletes existing `myenv/` and recreates it  

---

### 5. Dry‑Run Mode

```bash
python3 run_auto_setup.py -f your_script.py -l requirements.txt --dry-run
```

- Logs every intended action without changing anything  

---

### 6. Run Unit Tests

```bash
python3 run_auto_setup.py --test
```

- Executes built‑in tests (e.g., file‑existence checks)  

---

## 📄 Logging

All actions are logged to **auto_setup.log** _and_ echoed in the terminal.

---

## ⚙️ Customization

- Change virtual‑env folder:

```bash
export VENV_DIR="custom_env"
```

- Make the script executable:

```bash
chmod +x run_auto_setup.py
```

---

## 📬 Feedback & Contributions

Feel free to open issues or submit pull requests for improvements!

