# SOC – IoT Project Library

A separate Flask website for SOC classroom teaching. It is independent of the Exam Dashboard.

## Run on Windows
1. Extract the ZIP.
2. Open Command Prompt inside `SOC_IoT_Project_Library`.
3. Install: `python -m pip install -r requirements.txt`
4. Run: `python app.py`
5. Open: http://127.0.0.1:5000

## Admin
Open http://127.0.0.1:5000/admin/login
Default password: `socadmin123`

Before using on a shared/public network, set a strong password and secret key:
```bat
set SOC_ADMIN_PASSWORD=your-new-password
set SOC_SECRET_KEY=your-long-random-secret
python app.py
```

## Project content
The admin form supports title, summary, objective, equipment (one item per line), project photo, circuit diagram, pin-to-pin connections (one per line), working principle, source code, applications, precautions and teaching notes.

Project text is stored in `data/projects.json`; uploaded images are in `static/uploads/`. Back up both folders.

This starter is intended for local/classroom use. For public internet deployment, use HTTPS and a production WSGI server, not Flask's development server.
