```markdown
# BACK (RipesVapes) — Local & Deploy Notes

Local quick test:
1. Create venv:
   - python3 -m venv env
   - source env/bin/activate   (Windows: env\Scripts\activate)
2. Install dependencies:
   - pip install -r requirements.txt
3. Run dev server:
   - python scanner.py
   - Open http://127.0.0.1:5000/ to view site and test /verify endpoint.

Production with gunicorn:
- Start command (used by hosting): `gunicorn scanner:app -b 0.0.0.0:$PORT`

Notes:
- scanner.py expects `serials.csv` in the same folder and `templates/index.html` under BACK/templates.
- If you move serials.csv out of the repo for security, update scanner.py to load it from an environment path.
```