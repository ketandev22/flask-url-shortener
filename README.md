# Flask URL Shortener

A lightweight, minimal, and self-hosted URL shortener web application built using **Python** and the **Flask** framework. It generates unique, compact links and saves data locally using a JSON database.

##  Features

- **Instant URL Shortening:** Generates a random 6-character alphanumeric short code for any given URL.
- **Automatic Protocol Fixing:** Automatically prepends `https://` if the user forgets to type the protocol.
- **Persistent Data Storage:** Saves mappings locally in a `urls.json` file so links survive application restarts.
- **Collision Resistance:** Checks against existing data to ensure short codes never conflict.
- **Clean Redirections:** Performs standard HTTP redirects when visitors visit a short link.

##  Tech Stack

- **Backend:** Python 3.x, Flask
- **Database:** Local JSON storage (`urls.json`)

##  Project Structure

```text
flask-url-shortener/
├── app.py                # Main Flask application file
├── urls.json             # Automatically generated data file
└── templates/
    └── index.html        # Front-end UI (Form for submitting URLs)
```

##  Installation & Setup

Follow these steps to run the application locally on your machine:

### 1. Clone the repository
```bash
git clone https://github.com
cd flask-url-shortener
```

### 2. Set up a virtual environment (Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install flask
```

### 4. Create the required templates folder
Flask looks for HTML files in a `templates/` folder. Ensure you create a basic `index.html` inside it:
```bash
mkdir templates
```

### 5. Run the application
```bash
python app.py
```
The application will launch in debug mode on **`http://127.0.0.1:8000`**.

##  Roadmap & Future Improvements

- Add an elegant CSS frontend layout.
- Move from JSON storage to a relational database like SQLite for production safety.
- Include a analytics tracker to count total clicks per link.
- Introduce custom short code names instead of random characters.
