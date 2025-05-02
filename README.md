# 🎉 Birthday Email Bot 🎂

A simple Python script that automatically sends birthday emails to people whose birthdays are today, using data from a CSV file and randomly selected letter templates. 💌

## ✨ Features

* 📅 Reads birthday data from `birthdays.csv`
* 🔍 Matches today's date with birthday records
* 🧾 Randomly selects one of the letter templates
* 📬 Sends a personalized birthday email using Gmail SMTP

## 📁 Files

* `main.py`: Main script to send birthday emails.
* `birthdays.csv`: CSV file containing birthday data with columns: `name`, `email`, `year`, `month`, `day`.
* `letter_templates/`: Folder containing text files (`letter_1.txt` to `letter_5.txt`) with placeholders like `[NAME]`.

## ⚙️ Requirements

* 🐍 Python 3.x
* 🧮 pandas

Install dependencies:

```bash
pip install pandas
```

## 🛠️ Setup

1. **✉️ Email Configuration**:

   * Replace the `EMAIL_ADDRESS` and `EMAIL_PASSWORD` in `main.py` with your actual Gmail credentials.
   * For security, use [App Passwords 🔐](https://support.google.com/accounts/answer/185833?hl=en) instead of your actual Gmail password.

2. **📊 Create birthday CSV**:
   Example format:

   ```csv
   name,email,year,month,day
   John Doe,johndoe@example.com,1990,5,3
   Jane Smith,janesmith@example.com,1985,12,25
   ```

3. **📝 Create letter templates**:
   Each template (e.g. `letter_1.txt`) should contain a placeholder `[NAME]`, e.g.:

   ```
   Dear [NAME],

   Happy Birthday! Have a wonderful year ahead!
   ```

## ▶️ Running the Script

```bash
python main.py
```

If today's date matches any entry in `birthdays.csv`, a birthday email will be sent to the corresponding person. 🎯

## 🔒 Security Notice

Avoid hardcoding credentials in production. Use environment variables or a secure credentials store. 🛡️

## 🪪 License

MIT License 🧾
